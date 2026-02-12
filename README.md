# Exa MCP Server

A remote MCP server for AI-powered web search, code search, and research tools. Exa provides real-time web search capabilities with clean, ready-to-use content extraction.

## Setup

### Using tool CLI

Install the CLI from https://github.com/zerocore-ai/tool-cli

```bash
# Install from tool.store
tool install library/exa
```

```bash
# Configure your API key
tool config set library/exa api_key=YOUR_EXA_API_KEY
```

```bash
# View available tools
tool info library/exa
```

```bash
# Search the web
tool call library/exa -m web_search_exa -p query="latest AI developments"
```

```bash
# Find code examples
tool call library/exa -m get_code_context_exa -p query="React hooks best practices"
```

```bash
# Research a company
tool call library/exa -m company_research_exa -p companyName="OpenAI"
```

### Authentication

Exa MCP uses API key authentication. Get your API key from https://dashboard.exa.ai/api-keys

**Connection endpoint:**
- HTTP: `https://mcp.exa.ai/mcp`

## Tools

### `web_search_exa`

Search the web for any topic and get clean, ready-to-use content.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | Websearch query |
| `numResults` | number | No | Number of search results to return (default: 10) |
| `livecrawl` | string | No | Live crawl mode - 'fallback', 'always', or 'never' |
| `type` | string | No | Search type - 'auto' (default) or 'fast' |
| `contextMaxCharacters` | number | No | Maximum characters for context string optimized for LLMs |

### `company_research_exa`

Research any company to get business information, news, and insights.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `companyName` | string | Yes | Name of the company to research |
| `numResults` | number | No | Number of search results to return (default: 10) |

### `get_code_context_exa`

Find code examples, documentation, and programming solutions from GitHub, Stack Overflow, and docs.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | Search query to find relevant context for APIs, Libraries, and frameworks |
| `tokensNum` | number | No | Number of tokens to return (1000-50000, default: 10000) |

## Prompts

### `web_search_help`

Get help with web search using Exa.

### `code_search_help`

Get help finding code examples and documentation.

## Resources

### `exa://tools/list`

List of available Exa tools and their descriptions.

## License

Apache-2.0

## References

- https://exa.ai
- https://exa.ai/docs/reference/exa-mcp
- https://github.com/exa-labs/exa-mcp-server
