# Instalação rápida

Tribunal TRT22: Consulta Processual é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_tribunal_trt22_processo`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Tribunal TRT22: Consulta Processual` / `https://api.mcp.ai/p_tribunal_trt22_processo`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "tribunal_trt22_processo": { "type": "http", "url": "https://api.mcp.ai/p_tribunal_trt22_processo" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=tribunal_trt22_processo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF90cmlidW5hbF90cnQyMl9wcm9jZXNzbyJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "tribunal_trt22_processo": { "url": "https://api.mcp.ai/p_tribunal_trt22_processo" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=tribunal_trt22_processo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_tribunal_trt22_processo%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "tribunal_trt22_processo": { "type": "http", "url": "https://api.mcp.ai/p_tribunal_trt22_processo" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_tribunal_trt22_processo
```

Dúvidas? [tribunal_trt22_processo@mcp.ai](mailto:tribunal_trt22_processo@mcp.ai)
