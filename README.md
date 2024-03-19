# kafka-pipeline

## Real-time Stock Market Simulation with Kafka and AWS
This project simulates real-time stock market events using Python, Kafka, and AWS services. Here's an overview of the architecture:

Static Dataset: We have a static dataset stored on our local machine, serving as the source data for the simulation.

Producer Code: Python code is written to simulate real-time stock market events. It reads data from the static dataset. The produced events are sent to Kafka brokers.

Kafka Installation: Kafka is installed on an EC2 instance launched from AWS. This setup allows Kafka to handle messaging between producers and consumers efficiently.

Consumer Code: Another Python code reads data from Kafka brokers. It consumes the simulated stock market events  and introduces delays to mimic real-time behavior. Then pushes them into Amazon S3 buckets.

AWS Glue Crawler: A Glue crawler is employed to crawl the S3 buckets where the stock market data is stored. The crawler analyzes the data, infers the schema, and builds a catalog of the data structures. This catalog is known as the AWS Glue Catalog.

AWS Athena: With the Glue catalog in place, we can query the data stored in S3 using Athena. Athena enables us to run SQL queries against the data in S3 without needing to set up and manage a database infrastructure.

This architecture provides a scalable and efficient way to simulate and process real-time stock market data, store it securely, and make it queryable for analysis using Athena. Leveraging AWS services ensures flexibility and scalability as our needs evolve.

## Acknowledgement
[Youtuber Darshil Parmar](https://www.youtube.com/@DarshilParmar)

