# 🚀 **We’ve just launched our new MCP server!**

If you're building or using AI agents, you can now plug our web scraping API directly into your autonomous workflows. Just add the following to your MCP config:

```
{
  "mcpServers": {
    "web-scraping-api-by-instantapi-ai": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://web-scraping-api-by-instantapi-ai.help-052.workers.dev/sse",
        "--header",
        "Authorization:${AUTH_HEADER}"
      ],
      "env": {
        "AUTH_HEADER": "Bearer <YOUR_API_KEY>"
      }
    }
  }
}
```

🔐 Just replace <YOUR_API_KEY> with your API key from InstantAPI.ai. Sign up for your own API key here: https://web.instantapi.ai/#pricing-03-254921

Once connected, your AI agent can automatically invoke any of our scraping endpoints—/scrape, /links, /next, /search—to complete complex web data tasks, without needing any HTML selectors or manual logic.

🧠 Example real-world task from a user:

```
Go to https://www.domain.com.au/sale/bowral-nsw-2576/?bedrooms=1-any&bathrooms=1-any&excludeunderoffer=1&establishedtype=established&sort=dateupdated-desc
Extract each property link.
For each, get the full physical address and how many days since it was listed. If not known, assume 0 (today).
Keep paginating until no properties are listed in the last 7 days.
Return all matching addresses.
```

✅ The agent completed the task autonomously—scraping new leads for a mortgage broker with zero code written.

If you’re building AI workflows, this massively cuts down on glue code and edge case handling. Just give your agent a goal and let it fetch the data.
