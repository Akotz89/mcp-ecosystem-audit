# MCP Server Directory

A curated list of MCP server implementations, audited for quality and compatibility.

## Official Servers

| Server | Maintainer | Transport | Stars | Status |
|--------|-----------|-----------|-------|--------|
| [GitHub MCP](https://github.com/github/github-mcp-server) | GitHub | HTTP | 15k+ | ✅ Active |
| [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) | Anthropic | All | 5k+ | ✅ Active |
| [Python SDK](https://github.com/modelcontextprotocol/python-sdk) | Anthropic | All | 4k+ | ✅ Active |

## Community Servers

| Server | Purpose | Transport | Notes |
|--------|---------|-----------|-------|
| Context7 | Library documentation | HTTP | Fast lookups |
| Markdownify | File/web conversion | stdio/HTTP | 11 conversion tools |
| Mem0 | Persistent memory | HTTP | Vector + graph storage |
| Task Manager | Project management | stdio/HTTP | Dependency tracking |
| Chroma | Vector database | stdio | Embeddings storage |

## Transport Compatibility Matrix

| Server | stdio | SSE | Streamable HTTP |
|--------|-------|-----|----------------|
| GitHub MCP | ❌ | ❌ | ✅ |
| Context7 | ❌ | ❌ | ✅ |
| Markdownify | ✅ | ❌ | ✅ (wrapped) |
| Task Manager | ✅ | ❌ | ✅ (supergateway) |
| Mem0 | ❌ | ❌ | ✅ (native Python) |
