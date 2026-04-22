# MCP Protocol Overview

## What is MCP?
The Model Context Protocol (MCP) is an open standard that enables AI assistants to connect with external data sources and tools. Originally developed by Anthropic, it provides a standardized way for LLMs to interact with the world.

## Transport Types

### 1. stdio (Standard I/O)
The original transport — communicates via stdin/stdout pipes. Best for local processes.

### 2. SSE (Server-Sent Events) — Deprecated
HTTP-based transport using SSE for server→client messages. Being phased out in favor of Streamable HTTP.

### 3. Streamable HTTP (Current)
The recommended HTTP transport as of MCP spec 2025-03-26. Uses `StreamableHTTPServerTransport` from the TypeScript SDK.

```typescript
import { StreamableHTTPServerTransport } from '@modelcontextprotocol/sdk/server/streamableHttp.js';

const transport = new StreamableHTTPServerTransport({
  sessionIdGenerator: () => randomUUID(),
});
```

## Protocol Version
Current: `2024-11-05` (protocol version negotiated during initialize handshake)

## SDK Versions
- TypeScript SDK: v1.29.0 (2026-03-30)
- Python SDK: v1.8.0

## Key Concepts
- **Tools**: Functions the server exposes for the client to call
- **Resources**: Data the server can provide (files, database records)
- **Prompts**: Template prompts the server can offer
- **Sampling**: Server-initiated LLM requests (client capability)
