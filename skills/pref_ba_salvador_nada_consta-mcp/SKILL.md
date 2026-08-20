---
name: pref_ba_salvador_nada_consta-mcp
description: Skill da REST API do Prefeitura BA Salvador: Nada Consta na MCP.AI: 1 endpoint em /api/pref_ba_salvador_nada_consta. Prefeitura BA Salvador: Nada Consta, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Prefeitura BA Salvador: Nada Consta — REST API skill

Você tem acesso à **Prefeitura BA Salvador: Nada Consta** REST API na MCP.AI.

> Prefeitura BA Salvador: Nada Consta, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pref_ba_salvador_nada_consta
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
curl -X POST https://api.mcp.ai/api/pref_ba_salvador_nada_consta/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"renavam":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pref_ba_salvador_nada_consta/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pref_ba_salvador_nada_consta_consultar`

Prefeitura BA Salvador: Nada Consta, consulta em fonte oficial. _(POST /api/pref_ba_salvador_nada_consta/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `renavam` | string | Sim | Parâmetro de consulta "renavam". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pref_ba_salvador_nada_consta` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
