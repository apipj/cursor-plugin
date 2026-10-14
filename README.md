# apipj for Cursor: Brazilian CNPJ lookup (API CNPJ gratuita)

[![Install in Cursor](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/install-mcp?name=apipj&config=eyJ1cmwiOiJodHRwczovL2FwaXBqLmNvbS5ici9tY3AifQ==) [![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_apipj_MCP-0098FF?logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect/mcp/install?name=apipj&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapipj.com.br%2Fmcp%22%7D)

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
