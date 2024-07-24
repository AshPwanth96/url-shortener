Go URL Shortener Service
A simple URL shortener service implemented in Go, using github.com/go-chi/chi/v5 router and github.com/lithammer/shortuuid/v4 for short URL generation.

Features
Shorten URLs: Create short URLs by submitting a URL parameter via POST /short-it.
Redirect: Redirect to original URLs using short keys via GET /short/{key}.
Concurrency-Safe: Uses sync.Mutex for managing concurrent access to URL mappings.
Logging: Integrated logging to track operations and errors for enhanced reliability.
Getting Started
Prerequisites
Go (version 1.17 or higher) installed
Dependencies: github.com/go-chi/chi/v5 and github.com/lithammer/shortuuid/v4
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/AshPwanth96/url-shortener.git
cd url-shortener-go
Build and run the application:

bash
Copy code
go build -o url-shortener .
./url-shortener
Access the application at http://localhost:3000.

Usage
Shorten a URL:

Send a POST request to http://localhost:3000/short-it with a URL parameter:

bash
Copy code
curl -X POST -d "URL=https://google.com" http://localhost:3000/short-it
Redirect to original URL:

Use a browser or curl to access short URLs created:

bash
Copy code
curl -v http://localhost:3000/short/{key}
