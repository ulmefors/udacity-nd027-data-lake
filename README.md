# udacity-nd027-data-lake

Project submission for Udacity Data Engineering Nanodegree - Data Lake

## Summary

This project combines song listen log files with song metadata to facilitate analytics. JSON data is copied from an S3 bucket and processed using Apached Spark with the Python API. The data is organized into a star schema with fact and dimension tables. Analytics queries on the ` songplays` fact table are straightforward, and additional fields can be easily accessed in the four dimension tables `users`, `songs`, `artists`, and `time`. A star schema is suitable for this application since denormalization is easy, queries can be kept simple, and aggregations are fast.

## Install

```bash
$ unzip data/log_data.zip -d data
$ unzip data/song_data.zip -d data
$ mkdir output
```

```bash
$ pip install -r requirements.txt
```

## Run

1. Set environment variables `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`.
2. Create an S3 bucket and replace the `output_data` variable in the `main()` function with `s3a://<bucket name>/`, or uncomment the line below to run locally.

**Run ETL pipeline**

```bash
$ python etl.py
```