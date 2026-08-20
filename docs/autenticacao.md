# Autenticação

Prefeitura BA Salvador: Nada Consta usa um único endpoint público (`https://api.mcp.ai/p_pref_ba_salvador_nada_consta`).

Dois fluxos, escolhidos automaticamente pelo cliente:

- **OAuth 2.1** (recomendado, cliente moderno) — browser abre na 1ª chamada, login via magic-link, token rotaciona sozinho, nunca passa pelo chat.
- **agent-auth** (cliente sem OAuth) — o agente expõe a tool `authenticate(token)`. Você abre `https://app.mcp.ai/agent-auth`, faz login, copia o JWT e cola no chat. ⚠️ o JWT passa pelo provedor LLM — rotacione periodicamente.

Config do cliente nos dois casos:
```json
{ "mcpServers": { "pref_ba_salvador_nada_consta": { "url": "https://api.mcp.ai/p_pref_ba_salvador_nada_consta" } } }
```
