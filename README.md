# App Overview - Fibonacci Sequence

## Client

Simple React app that takes an index number, and returns the corresponding Fibonacci number at that index. Also keeps a list of all the index numbers so far requested. Nothing fancy.

## Server

Express app connects to Redis and Postgres to handle storing of data and logic execution. Set up endpoints for handling client requests and storing data.

## Worker

This is where the Fibonacci function logic is ran via Redis. Given an index of the sequence, this will send back the corresponding Fib value.

## Nginx

We are using Nginx to handle routing for both the Client and Server. Setup of the `default.conf` file tells any request with a URI beginning with `/api` to be routed to the Server, else goes to Client

---

## Purpose of this excercise?

1. Learning to build a Multi-Container application in development using Docker, React, Node, Postgres, Redis and Nginx

2. To implement continuous integration with Github and Travis CI, then pushing our images to Docker Hub

3. Finally, put the app in to production on an AWS Elastic Beanstalk instance. In production, Postgres and Redis are replaced with AWS RDS and ElastiCache.

4. Learn how to link multiple containers using `Dockerrun.aws.json` file.

---

## Takeaways

- Nginx usage, port mapping, routing, proxys

- Trouble shooting docker images and builds

- Implementation of environment variables for DBs and AWS

- Better understanding of Travis CI and best deployment and continuous integration practices

- Wiring up Elastic Beanstalk instance and connecting an RDS and ElastiCache with a custom security group
