# Project: Data Modeling with Postgres

## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.

## Project Description
In this project, you'll apply what you've learned on data modeling with Postgres and build an ETL pipeline using Python. To complete the project, you will need to define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

## Document Process
1. Discuss the purpose of this database in the context of the startup, Sparkify, and their analytical goals.
2. State and justify your database schema design and ETL pipeline.
3. [Optional] Provide example queries and results for song play analysis.

The Star Schema will be utilized for data modeling, featuring a central fact table for songplays events and linked to four dimension tables: songs, artists, users, and time, each with primary keys referenced by the fact table.

The rationale for choosing a relational database for this scenario includes:

The data format is pre-determined, allowing for precise extraction and transformation from the JSON sources.
The data volume is manageable without the need for big data solutions.
This schema enhances efficient data summarization and analysis.
SQL is a suitable and powerful tool for the required analysis tasks.
The need to perform JOINS in queries is well-supported by relational databases.

### The project consists of seven key files:

create_tables.py: This script is used to drop existing tables and create new ones. It should be executed to refresh the tables before running the ETL scripts.
etl.ipynb: This Jupyter notebook is a step-by-step guide for processing a single file from song_data and log_data and for inserting the data into the tables. It provides a detailed ETL process for each table.
etl.py: This script processes all files from song_data and log_data and populates the tables. It should be completed using the ETL notebook as a reference.
README.md: This markdown file offers an overview and discussion of the project.
sql_queries.py: This file contains all the SQL queries used and is imported by the aforementioned scripts.
test.ipynb: This Jupyter notebook displays the first few rows from each table as a quick way to inspect the database contents.

### How to Run

Run create_tables.py to create the database and tables.
Run etl.py to process for loading, extracting and inserting the data.
Run test.ipynb to confirm the creation of database and columns.