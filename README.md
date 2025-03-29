# Redis Clone

A lightweight implementation of a Redis-like server in Python using the `asyncio` library. This project supports basic Redis commands like `PING`, `ECHO`, `SET`, and `GET`, as well as key expiration features.

---

## Features

- **Commands Supported**:
  - **PING**: Test connectivity with `PONG`.
  - **ECHO**: Echo back the provided message.
  - **SET**: Store a key-value pair in the in-memory store.
    - Optional expiration using `EX` (seconds) or `PX` (milliseconds).
  - **GET**: Retrieve the value of a key.
- **Key Expiry**:
  - Expiration for keys can be set with `EX` or `PX` during the `SET` operation.
- **RESP Protocol**:
  - Implements the Redis Serialization Protocol (RESP) for parsing and sending responses.
- **Asynchronous**:
  - Built with `asyncio` for handling multiple connections concurrently.
- **Replication**:
  - Implements master-replica communication using the `REPLCONF` and `PSYNC` protocols.
- **Persistence**:
  - Data persistence is supported for reliable storage between sessions.
- **Concurrency**:
  - Efficient handling of multiple clients using Go’s goroutines and synchronization primitives.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/redis-clone.git
2. Navigate to the project directory:
   ```bash
   cd redis-clone
3. Run the server:
   ```bash
   python app/main.py

## Usage

- **Running the server**:
  - **PING**: Test connectivity with `PONG`.
  - **ECHO**: Echo back the provided message.
  - **SET**: Store a key-value pair in the in-memory store.
    - Optional expiration using `EX` (seconds) or `PX` (milliseconds).
  - **GET**: Retrieve the value of a key.
  - **REPLCONF**: Handle replica configuration.
  - **PSYNC**: Synchronize data between master and replica.
