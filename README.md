# Golang Service Sample

This repository contains a sample REST service implemented in Golang.

## Quick Start Guide

1. Download and install todos golang service sample:

   ```bash
   go get github.com/imesh/golang-service-sample/todos
   ```

2. Start the todos service:

   ```bash
   todos
   ```

3. Make following HTTP requests:

   ```bash
   curl -v http://localhost:8080/
   > GET / HTTP/1.1
   > Host: localhost:8080
   > User-Agent: curl/7.54.0
   > Accept: */*
   >
   < HTTP/1.1 200 OK
   < Date: Tue, 06 Mar 2018 09:49:29 GMT
   < Content-Length: 9
   < Content-Type: text/plain; charset=utf-8
   <
   Welcome!
   ```

   ```bash
   curl -v http://localhost:8080/todos
   ...
   > GET /todos HTTP/1.1
   > Host: localhost:8080
   > User-Agent: curl/7.54.0
   > Accept: */*
   >
   < HTTP/1.1 200 OK
   < Date: Tue, 06 Mar 2018 09:47:45 GMT
   < Content-Length: 149
   < Content-Type: text/plain; charset=utf-8
   <
   [{"name":"Write presentation","completed":false,"due":"0001-01-01T00:00:00Z"},{"name":"Host meetup","completed":false,"due":"0001-01-01T00:00:00Z"}]
   ```

   ```bash
   curl -v http://localhost:8080/todos/foo
   > GET /todos/foo HTTP/1.1
   > Host: localhost:8080
   > User-Agent: curl/7.54.0
   > Accept: */*
   >
   < HTTP/1.1 200 OK
   < Date: Tue, 06 Mar 2018 09:50:03 GMT
   < Content-Length: 15
   < Content-Type: text/plain; charset=utf-8
   <
   Todo show: foo
   ```

## References

- [Making a RESTful JSON API in Go](https://thenewstack.io/make-a-restful-json-api-go/), The New Stack
