# MCP Server Setup Guide

## Prerequisites
- Docker Engine 24+
- Node.js 22+ (for SDK development)
- Python 3.12+ (for Python-based servers)

## Quick Start

```bash
# Clone the MCP TypeScript SDK
git clone https://github.com/modelcontextprotocol/typescript-sdk.git
cd typescript-sdk
npm install
```

## Transport Configuration

### Streamable HTTP (Recommended)
```typescript
import { StreamableHTTPServerTransport } from '@modelcontextprotocol/sdk/server/streamableHttp.js';
import express from 'express';

const app = express();
const transport = new StreamableHTTPServerTransport({ sessionIdGenerator: () => randomUUID() });
```

### stdio (Local Development)
```typescript
import { StdioServerTransport } from '@modelcontextprotocol/sdk/server/stdio.js';
const transport = new StdioServerTransport();
```
