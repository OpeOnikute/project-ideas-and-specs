# Pigeon

## Overview
A bunch of serverless functions that work together to schedule Twitter messages. Inspired by shalvah's [this_vid](twitter.com/this_vid).

## Architecture
- Serverless.

## Components 
- Message Scheduler Function.
- Task queue (RabbitMQ, because of it's ability to delay tasks).
- Message Delivery Function.

## User Features
- Bot to accept message requests.
- Message management (cancel, retry etc).
- Admin message management.