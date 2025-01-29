# Java Web Server Samples

This repository demonstrates three server implementations in Java:

- SingleThreaded: one connection at a time
- Multithreaded: one thread per connection
- ThreadPool: fixed-size thread pool using ExecutorService

## Structure
```
java-webserver/
  SingleThreaded/
    Server.java
    Client.java
  Multithreaded/
    Server.java
    Client.java
  ThreadPool/
    Server.java
```

## Requirements
- Java 8+ (javac, java in PATH)

## How to run

### SingleThreaded
Terminal 1:
```
cd SingleThreaded
javac Server.java
java Server
```
Terminal 2:
```
cd SingleThreaded
javac Client.java
java Client
```

### Multithreaded
Terminal 1 (server):
```
cd Multithreaded
javac Server.java
java Server
```
Terminal 2 (client spawns 100 connections):
```
cd Multithreaded
javac Client.java
java Client
```

### ThreadPool
Terminal (server only):
```
cd ThreadPool
javac Server.java
java Server
```
You can reuse `Multithreaded/Client.java` to create load against the thread-pool server.
