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
| `query` | string | Yes | The search query to find relevant web content |
| `numResults` | number | No | Number of results to return (default: 10) |

### `get_code_context_exa`

Find code examples, documentation, and programming solutions from GitHub, Stack Overflow, and docs.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | The code-related query to search for |
| `numResults` | number | No | Number of results to return (default: 10) |

### `company_research_exa`

Research any company to get business information, news, and insights.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `companyName` | string | Yes | The name of the company to research |

### `deep_search_exa`

Deep web search with smart query expansion and high-quality summaries for each result.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | The search query for deep web search |
| `numResults` | number | No | Number of results to return (default: 10) |

### `crawling_exa`

Get the full content of a specific webpage from a known URL.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `url` | string | Yes | The URL of the webpage to crawl |

### `linkedin_search_exa`

Search LinkedIn for companies and people using Exa AI.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | The search query (company names, person names, or LinkedIn URLs) |
| `numResults` | number | No | Number of results to return (default: 10) |

### `deep_researcher_start`

Start an AI research agent that searches, reads, and writes a detailed report.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `query` | string | Yes | The research question or topic for the AI agent |

### `deep_researcher_check`

Check status and get results from a deep research task.

**Input:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `taskId` | string | Yes | The task ID returned from deep_researcher_start |

## License

Apache-2.0

## References

- https://exa.ai
- https://exa.ai/docs/reference/exa-mcp
- https://github.com/exa-labs/exa-mcp-server
