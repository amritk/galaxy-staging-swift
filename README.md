# DemoApiScalarGalaxy Swift API Library

This package provides convenient access to the DemoApiScalarGalaxy REST API from Swift applications.
It is generated from your OpenAPI document with typed Codable models, async resource methods, pagination helpers, and Swift 5.10+ support.

The full generated API reference is available in `api.md` and the operation inventory is available in `reference.md`.

## Installation

Add this package to your Swift Package Manager dependencies:

```swift
.package(path: ".")
```

## Usage

Instantiate the generated client and call async methods from resource clients.

```swift
import DemoApiScalarGalaxy

let client = DemoApiScalarGalaxy()
let response = try await client.planets.list()
```

## Request and Response Types

Request params and response bodies are generated as Swift structs and enums using `Codable` and `Sendable` where practical.
Resource methods use `async throws` and return typed models, pages, streams, or `Data` depending on the OpenAPI response.

## Handling Errors

Non-success responses throw generated API errors that expose status code, headers, raw body, and request id metadata when available.
Transport failures are surfaced through Swift error handling.

## Retries and Timeouts

The runtime supports client-level and per-request timeout, retry, header, query, base URL, and idempotency options.
Retryable responses honor `Retry-After` before exponential backoff.

## Pagination

Paginated operations expose page helpers and next-page metadata when pagination is described by the OpenAPI document.

## Raw Responses and Custom Requests

Raw response helpers are available when callers need status, headers, or unparsed response data.
Per-request options provide an escape hatch for extra headers and query params.

## Requirements

Swift 5.10+ with macOS 13+ or iOS 16+.
