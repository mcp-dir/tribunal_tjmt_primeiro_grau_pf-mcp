---
name: tribunal_tjmt_primeiro_grau_pf-mcp
description: Skill da REST API do Tribunal TJMT: Certidão do 1º Grau (Pessoa Física) na MCP.AI: 1 endpoint em /api/tribunal_tjmt_primeiro_grau_pf. Tribunal TJMT: Certidão do 1º Grau (Pessoa Física), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Tribunal TJMT: Certidão do 1º Grau (Pessoa Física) — REST API skill

Você tem acesso à **Tribunal TJMT: Certidão do 1º Grau (Pessoa Física)** REST API na MCP.AI.

> Tribunal TJMT: Certidão do 1º Grau (Pessoa Física), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/tribunal_tjmt_primeiro_grau_pf
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/tribunal_tjmt_primeiro_grau_pf/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"cpf":"...","birthdate":"...","tipo_certidao":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/tribunal_tjmt_primeiro_grau_pf/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `tribunal_tjmt_primeiro_grau_pf_consultar`

Tribunal TJMT: Certidão do 1º Grau (Pessoa Física), consulta em fonte oficial. _(POST /api/tribunal_tjmt_primeiro_grau_pf/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Sim | Parâmetro de consulta "cpf". |
| `birthdate` | string | Sim | Parâmetro de consulta "birthdate". |
| `tipo_certidao` | string | Sim | Parâmetro de consulta "tipo_certidao". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_tribunal_tjmt_primeiro_grau_pf` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
