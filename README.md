# Sourcegraph MCP Server

This registry entry represents the Sourcegraph MCP server for a Sourcegraph instance. 
It can be configured against Sourcegraph Cloud or a private Sourcegraph deployment, so users can connect MCP-compatible clients to their own Sourcegraph server.

At a high level, the Sourcegraph MCP server gives agents and applications access to Sourcegraph code search and code intelligence capabilities through a standard MCP interface. 
That includes common workflows such as repository discovery, file reads, keyword and semantic search, symbol navigation, references, and code-change exploration.

## Configuration

Configure the server with the hostname of your Sourcegraph instance. This entry uses the standard Sourcegraph MCP endpoint:

`https://{sourcegraph_hostname}/.api/mcp`

For private Sourcegraph instances, set `sourcegraph_hostname` to your internal or company-hosted Sourcegraph server hostname.

Authentication is handled by Sourcegraph. Depending on the MCP client, this is typically done with browser-based OAuth or a Sourcegraph access token. This MCP config defaults to OAuth.

## Notes

This README intentionally keeps client-specific setup details light because MCP integration steps can change over time. 
For the current Sourcegraph MCP server behavior, supported authentication modes, and client-specific setup instructions, see the official Sourcegraph documentation:

<https://sourcegraph.com/docs/api/mcp#sourcegraph-mcp-server>
