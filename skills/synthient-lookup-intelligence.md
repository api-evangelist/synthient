---
name: synthient-lookup-intelligence
description: Retrieve honeypot intelligence for a domain, then look up providers for an IP address, and finally enrich multiple IP addresses in
  batch.
api: openapi/synthient-openapi.json
operations:
- domainLookup
- ipLookup
- lookupIpBatch
generated: '2026-09-28'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/synthient-openapi.json ; every operationId checked against the contract
---

# synthient-lookup-intelligence

Retrieve honeypot intelligence for a domain, then look up providers for an IP address, and finally enrich multiple IP addresses in batch.

## Steps

1. 1. Use `domainLookup` with path parameter `domain`.
2. 2. Use `ipLookup` with path parameter `ip_address`.
3. 3. Use `lookupIpBatch` with request body containing an array of IP addresses.

## Rules

- Auth: Include API key in header `X-Api-Key`.
- Rate limit: 100 requests per second; exceeding returns HTTP 429.
