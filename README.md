# AI Trust Tools

Tools that make content safe for AI agents, plus a few data and compliance tools. They run on [Apify](https://apify.com/bigochelo) and can be used from any MCP client, the Apify API, n8n, Make or Zapier. Pay per use; failed items are never charged.

## For AI agents and RAG

| Tool | What it does | Use it |
|---|---|---|
| MCP Tool Poisoning Scanner | Audits MCP servers for tool poisoning, hidden instructions and silent tool changes (rug pulls) | [Apify](https://apify.com/bigochelo/mcp-poisoning-scanner) |
| Safe Web Reader | Web pages, JavaScript sites and PDFs to clean Markdown, prompt-injection text removed and reported | [Apify](https://apify.com/bigochelo/safe-web-reader) |
| PDF to Markdown | PDFs to Markdown for RAG, with tables, heading-aware chunks and hidden-text detection | [Apify](https://apify.com/bigochelo/pdf-to-markdown-text-for-ai-rag) |
| OCR to Markdown | Scanned PDFs and images to Markdown, 26 languages | [Apify](https://apify.com/bigochelo/ocr-to-markdown) |

## Data and compliance

| Tool | What it does | Use it |
|---|---|---|
| Google Trends Scraper | Interest over time, by region and related queries for any keyword, plus **Trending now**: the searches spiking right now in any country | [Apify](https://apify.com/bigochelo/google-trends-scraper) |
| EAA Spain checker | Checks Spanish online shops in bulk for an accessibility statement (Ley 11/2023) and an AI notice on their chatbot (AI Act art. 50), with a traffic light and an explanation in Spanish | [Apify](https://apify.com/bigochelo/eaa-spain-compliance-checker) |

## Use from an MCP client

The MCP Tool Poisoning Scanner and Safe Web Reader are listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=marcepalacios12) as `io.github.marcepalacios12/mcp-poisoning-scanner` and `io.github.marcepalacios12/safe-web-reader`.

```json
{
  "mcpServers": {
    "ai-trust-tools": {
      "url": "https://mcp.apify.com/?tools=bigochelo/mcp-poisoning-scanner,bigochelo/safe-web-reader",
      "headers": { "Authorization": "Bearer <YOUR_APIFY_TOKEN>" }
    }
  }
}
```

Without the header, compatible clients sign you in with OAuth. Any of the tools above can be added to the `tools` list in the URL, e.g. `bigochelo/google-trends-scraper`. Usage is billed per event on your Apify account; failed items are not charged.

## Support
Open an issue in this repository or on the tool's Apify page.
