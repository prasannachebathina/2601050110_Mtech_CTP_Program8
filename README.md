# Asynchronous Web Crawler

## Aim

To develop an asynchronous web crawler using `asyncio` and `aiohttp` with a retry mechanism and compare its performance with a sequential web crawler.

## Technologies Used

* Python
* asyncio
* aiohttp
* requests
* time

## Description

The project downloads web pages from multiple URLs.

Two approaches are implemented:

1. **Sequential Crawler** – downloads URLs one by one.
2. **Asynchronous Crawler** – downloads multiple URLs concurrently using `asyncio` and `aiohttp`.

A retry mechanism is added to handle temporary request failures.

## Procedure

1. Define a list of URLs.
2. Implement the sequential crawler.
3. Implement the asynchronous crawler.
4. Add retries for failed requests.
5. Measure execution time.
6. Compare sequential and asynchronous execution times.
7. Display the results.

## Input

A list of website URLs.

Example:

```text
https://example.com
https://www.python.org
https://www.google.com
```

## Output

The program displays the HTTP status of each URL and the execution time of both implementations.

Example:

```text
----- RESULT -----
Sequential Time : 1.52 seconds
Async Time      : 0.48 seconds
```

## Inference

The asynchronous crawler can handle multiple network requests concurrently and is generally faster for I/O-bound operations.

## Conclusion

The experiment demonstrates that asynchronous programming with `asyncio` and `aiohttp` can improve the efficiency of web crawling compared with sequential execution. The retry mechanism also improves reliability when temporary network failures occur.
