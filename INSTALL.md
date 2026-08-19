# Instalação rápida

Tribunal TJMT: Certidão do 1º Grau (Pessoa Física) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Tribunal TJMT: Certidão do 1º Grau (Pessoa Física)` / `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "tribunal_tjmt_primeiro_grau_pf": { "type": "http", "url": "https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=tribunal_tjmt_primeiro_grau_pf&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF90cmlidW5hbF90am10X3ByaW1laXJvX2dyYXVfcGYifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "tribunal_tjmt_primeiro_grau_pf": { "url": "https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=tribunal_tjmt_primeiro_grau_pf&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_tribunal_tjmt_primeiro_grau_pf%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "tribunal_tjmt_primeiro_grau_pf": { "type": "http", "url": "https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf
```

Dúvidas? [tribunal_tjmt_primeiro_grau_pf@mcp.ai](mailto:tribunal_tjmt_primeiro_grau_pf@mcp.ai)
