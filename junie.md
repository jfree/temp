# Junie


Go to Tools > Junie > MCP Settings and add the following block:

```
{
  "mcpServers": {
    "datadog": {
      "type": "http",
      "url": "https://mcp.datadoghq.com/api/unstable/mcp-server/mcp"
    }
  }
}
```

To enable product-specific tools, include the `toolsets` query parameter at the end of the endpoint URL. For example, this URL enables only APM and LLM Observability tools:

```
https://mcp.datadoghq.com/api/unstable/mcp-server/mcp?toolsets=apm,llmobs
```

You are prompted to login through OAuth. The status indicator in the settings displays a green tick when the connection is successful.