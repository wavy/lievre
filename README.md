# Lievre Project

Lievre is an experimental server implementation of AMQP 0.9.1 with RabbitMQ extensions in Rust.

Its primary use-case is for building integration tests for Rust projects using RabbitMQ. It can also be run standalone,
acting as a low-resource replacement of the RabbitMQ server.

## Overview

The purpose of Lievre is to be a light alternative to RabbitMQ, mainly to be used in prototypes or in integration
tests. It is not suitable to run in a production environment or as a drop-in replacement for RabbitMQ.

In other words, you can expect Lievre to support primary AMQP features:

- Authentication
- Connections and Multiplexing
- Exchanges and Queues
- Content ordering guarantees
- Error handling
- Persistence (in the standalone version)

It does not guarantee an implementation usually required in production systems, such as:

- High availability
- Federation
- Multiple protocols
- Plugins

The objective of this project is to achieve an implementation of AMQP 0.9.1 that respects the formal spec. We will
also try to implement as many [RabbitMQ extensions]() as possible, so long as they align with Lievre's use-cases.

## Crates

- `lievre`: The AMQP 0.9.1 server library.

- `lievre-standalone`: A binary application that runs the Lievre server in its own process.

- `lievre-live`: The library used to run Lievre in the same process as the client. Mainly used for integration tests.

## Resources

- [AMQP 0.9.1 Specification (PDF)](https://www.rabbitmq.com/resources/specs/amqp0-9-1.pdf)

## License

This project is licensed under MIT. It is developed by [Wavy Labs](https://github.com/WavyLabs/).
