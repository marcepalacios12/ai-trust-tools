# AI Trust Tools

Tools that make content safe for AI agents. They run on [Apify](https://apify.com/bigochelo) and can be used from any MCP client, the Apify API, n8n, Make or Zapier.

| Tool | What it does | Use it |
|---|---|---|
| MCP Tool Poisoning Scanner | Audits MCP servers for tool poisoning, hidden instructions and silent tool changes | [Apify](https://apify.com/bigochelo/mcp-poisoning-scanner) |
| Safe Web Reader | URL to clean Markdown with prompt-injection text removed | [Apify](https://apify.com/bigochelo/safe-web-reader) |
| PDF to Markdown | PDFs to Markdown for RAG, with hidden-text detection | [Apify](https://apify.com/bigochelo/pdf-to-markdown-text-for-ai-rag) |
| OCR to Markdown | Scanned PDFs and images to Markdown, 26 languages | [Apify](https://apify.com/bigochelo/ocr-to-markdown) |
| Google Trends Scraper | Google Trends data without an API key | [Apify](https://apify.com/bigochelo/google-trends-scraper) |

## Use from an MCP client

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

Without the header, compatible clients sign you in with OAuth. Usage is billed per event on your Apify account; failed items are not charged.

## Support
Open an issue in this repository or on the tool's Apify page.
