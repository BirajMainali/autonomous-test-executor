# 🤖 Collaborative Test Agent Configuration

This guide explains how to configure collaborative test agents using the **Model Context Protocol (MCP)**. These agents work together to fetch, execute, and report automated test cases.

---

## 📦 Configuration Format

Define the agents under the `mcpServers` key in your configuration file:

```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest"
      ]
    },
    "test-case-mcp-server": {
      "command": "uv",
      "args": [
        "--directory",
        "PATH_OF_CASE_MCP_SERVER",
        "run",
        "main.py"
      ],
      "env": {
        "executableDir": "CURRENT_PROJECT_CLONED_PATH"
      }
    }
  }
}
