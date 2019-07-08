# Rust Space API Implementation

[![Build Status](https://img.shields.io/travis/spaceapi-community/spaceapi-server-rs/master.svg)](https://travis-ci.org/spaceapi-community/spaceapi-server-rs)
[![Test Coverage](https://img.shields.io/coveralls/spaceapi-community/spaceapi-server-rs/master.svg)](https://coveralls.io/github/spaceapi-community/spaceapi-server-rs)
[![Crates.io Version](https://img.shields.io/crates/v/spaceapi-server.svg)](https://crates.io/crates/spaceapi-server)
[![Crates.io Downloads](https://img.shields.io/crates/d/spaceapi-server.svg)](https://crates.io/crates/spaceapi-server)
[![Dependency Status](https://dependencyci.com/github/spaceapi-community/spaceapi-server-rs/badge)](https://dependencyci.com/github/spaceapi-community/spaceapi-server-rs)
[![Clippy Linting Result](https://clippy.bashy.io/github/spaceapi-community/spaceapi-server-rs/master/badge.svg)](https://clippy.bashy.io/github/spaceapi-community/spaceapi-server-rs/master/log)

This is a library that allows an easy implementation of a
[SpaceAPI](https://spaceapi.io/) v0.13 server in Rust.

- Crate Documentation: https://docs.rs/spaceapi-server/
- Space API Reference: https://spacedirectory.org/pages/docs.html

## Requirements

 * Rust 1.31 or newer


## Usage

See the `examples` directory or our
[Status-Project](https://github.com/coredump-ch/status) for reference.

To run the examples from the project directory:

    $ cargo run --example simple


## Datastores

### Redis

To use the redis storage start the redis server:

    $ redis-server

(...or start it using your favorite init daemon.)

You can access the database with the `redis-cli` tool:

    % redis-cli
    127.0.0.1:6379> SET people_present 1
    OK
    127.0.0.1:6379> GET people_present
    "1"
    127.0.0.1:6379> KEYS *
    1) "people_present"

The values depend on your sensors configuration.


## Docs

You can build docs with `make docs`. Find them in the `target/doc/` directory.

## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in the work by you, as defined in the Apache-2.0
license, shall be dual licensed as above, without any additional terms or
conditions.
