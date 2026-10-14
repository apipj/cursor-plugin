# apipj for Cursor: Brazilian CNPJ lookup (API CNPJ gratuita)

Look up and validate Brazilian companies by CNPJ inside [Cursor](https://cursor.com), using Receita Federal open data through the [apipj](https://apipj.com.br) MCP server.

## What's included

- **MCP server** (`mcp.json`): `https://apipj.com.br/mcp`, Streamable HTTP.
  - `validar_cnpj` and `status_base` work without an account.
  - `consultar_cnpj` asks you to connect your apipj account (OAuth; Google sign-in works). The free plan includes 50,000 lookups per month.
- **Rule** (`rules/apipj-cnpj.mdc`): teaches the agent how to call the apipj REST API correctly (auth, 404 vs 429 handling, alphanumeric CNPJ, caching) when you write integration code.

## Manual install

Add to `~/.cursor/mcp.json` or `.cursor/mcp.json` in your project:

```json
{
  "mcpServers": {
    "apipj": { "url": "https://apipj.com.br/mcp" }
  }
}
```

## Em português

Consulte e valide CNPJ (inclusive o CNPJ alfanumérico) direto no Cursor, com os dados abertos da Receita Federal. Plano grátis com 50 mil consultas por mês: [crie sua conta](https://apipj.com.br/criar-conta). Guia completo: https://apipj.com.br/guias/consultar-cnpj-ia-mcp

## Links

- Docs: https://apipj.com.br/docs
- JavaScript/TypeScript client: https://www.npmjs.com/package/apipj
- Python client: https://pypi.org/project/apipj/
- MCP Registry: `br.com.apipj/cnpj`

License: MIT
