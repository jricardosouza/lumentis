# Claude MCP Configuration

This directory contains Model Context Protocol (MCP) configuration for Claude Code.

## Supabase MCP Server Setup

The project is configured to use Supabase MCP server for enhanced capabilities.

### Global Configuration

For Claude Code to access the MCP server globally, the configuration should be placed in `~/.claude.json`:

```bash
cat > ~/.claude.json << 'EOF'
{
  "mcpServers": {
    "supabase": {
      "type": "http",
      "url": "https://mcp.supabase.com/mcp?project_ref=sxohhtyzlgokwnlzbbrf"
    }
  }
}
EOF
```

### Security

Ensure the configuration file has restricted permissions:

```bash
chmod 600 ~/.claude.json
```

This ensures only the file owner can read and write the configuration.

### Verification

To verify the setup:

```bash
# Check file permissions and size
ls -lh ~/.claude.json

# Verify configuration content
cat ~/.claude.json
```

Expected permissions: `-rw-------` (600)

## Project Configuration

This directory also contains a local copy of the MCP configuration (`mcp.json`) for reference and version control purposes.

## More Information

- [Model Context Protocol Documentation](https://modelcontextprotocol.io/)
- [Supabase MCP Server](https://supabase.com/docs/guides/mcp)
