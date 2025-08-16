
# 🌐 Multithreaded Proxy Web Server in C

[![C](https://img.shields.io/badge/language-C-blue.svg)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Build](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-yellow.svg)](./LICENSE)
[![Contributions](https://img.shields.io/badge/contributions-welcome-orange.svg)]()

A simple yet efficient **multithreaded proxy web server** written in **C**.  
It handles multiple client requests concurrently using POSIX threads (`pthread`), supports basic HTTP request forwarding, and demonstrates low-level socket programming concepts.

---

## 🚀 Features
- Accepts and processes multiple client connections simultaneously.
- Forwards HTTP requests from clients to destination servers.
- Returns responses back to clients via proxy.
- Uses **pthreads** for concurrency.
- Implements non-blocking I/O and error handling.
- Supports basic logging of requests.

---

## 📂 Project Structure
```
├── proxy.c          # Main server implementation
├── proxy_parse.h    # HTTP request parsing utilities
├── proxy_parse.c    # Parsing logic implementation
├── Makefile         # Build instructions
└── README.md        # Documentation
```

---

## ⚙️ Requirements
- GCC or Clang compiler
- POSIX-compliant system (Linux/Unix/macOS)
- Basic networking libraries (`sys/socket.h`, `netinet/in.h`, etc.)

---

## 🛠️ Build Instructions
```bash
# Clone the repository
git clone https://github.com/hacketthadwin/Multithreaded-Proxy-Web-server.git
cd Multithreaded-Proxy-Web-server

# Compile
make
```

---

## ▶️ Usage
Run the proxy server on a chosen port:
```bash
./proxy <port>
```

Example:
```bash
./proxy 8080
```

Then configure your browser or system to use `localhost:8080` as the HTTP proxy.

---

## 📖 Example Workflow
1. Client (browser or curl) sends an HTTP request.
2. Proxy server accepts the connection.
3. A new thread is spawned to handle the request.
4. Proxy forwards the request to the target server.
5. Target server responds → proxy relays back to client.

---

## 🔧 Future Improvements
- Support for HTTPS (via CONNECT method).
- Caching frequently accessed pages.
- More detailed logging & monitoring.
- Load balancing strategies.

---

## 📜 License
This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
