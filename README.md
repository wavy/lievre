# Lievre Project

Lievre is an experimental implementation of AMQP 0.9.1 with RabbitMQ extensions. Its primary use-case is for
building integration tests for Rust projects using RabbitMQ. It can also be run standalone,
acting as a low-resource replacement of the RabbitMQ server.

## Architecture

Lievre is broken up in 3 crates:

* `lievre`: The AMQP 0.9.1 server library.

* `lievre-standalone`: The binary application used to run the Lievre server.

* `lievre-live`: The library used to run Lievre in the same process as the client. Mainly used for integration tests.

## License

This project is licensed under MIT. It is developed by [Wavy Labs](https://github.com/wavymedia/).
