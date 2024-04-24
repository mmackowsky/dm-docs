# Decision to Use Celery with Redis in the Project

Date: `2024-04-23`

## Status

Accepted

## Context

During the development of my application project, I recognize the need for implementing asynchronous background task handling. I aim to process tasks that do not require immediate execution in response to user requests. To achieve this, I am considering various tools and technologies that will enable me to effectively handle asynchronous tasks.

## Decision

After evaluating different options, I have decided to utilize Celery in conjunction with Redis as the mechanism for handling background tasks. Celery is a popular tool for managing asynchronous tasks in Python-based applications, providing flexibility, scalability, and reliability. Redis, on the other hand, will serve as the message broker for Celery, facilitating communication between the application and the background tasks.

## Consequences

- Scalability: Choosing Celery with Redis will allow me to easily scale the handling of asynchronous tasks as the application's load increases.
- Flexibility: Celery offers a wide range of features such as task scheduling, progress monitoring, and error handling, providing me with flexibility in handling various types of tasks.
- Configuration and Deployment: Configuring and deploying the Redis infrastructure and integrating it with Celery in my application will be necessary. This requires appropriate preparatory work and testing, but the benefits outweigh these efforts.

## Keywords

- Celery
- Redis
- Asynchronicity
