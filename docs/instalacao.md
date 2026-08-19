# Instalação detalhada

Tribunal TJMT: Certidão do 1º Grau (Pessoa Física) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.tribunal_tjmt_primeiro_grau_pf` (ou `servers.tribunal_tjmt_primeiro_grau_pf` no VS Code) do config do cliente e reinicie.
