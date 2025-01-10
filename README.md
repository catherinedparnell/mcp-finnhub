# Finnhub MCP Server

An MCP server to interface with Finnhub API.

### Tools

- `list_news`

  - List latest market news from Finnhub [market news endpoint](https://finnhub.io/docs/api/market-news)

- `get_market_data`

  - Get market data for a particular stock from [quote endpoint](https://finnhub.io/docs/api/quote)

- `get_basic_financials`

  - Get basic financials for a particular stock from [basic financials endpoint](https://finnhub.io/docs/api/company-basic-financials)

- `get_recommendation_trends`
  - Get recommendation trends for a particular stock from [recommendation trend endpoint](https://finnhub.io/docs/api/company-basic-financials)

## Configuration

1. Run `uv sync` to install the dependencies. To install `uv` follow the instructions [here](https://docs.astral.sh/uv/). Then do `source .venv/bin/activate`.

2. Setup the `.env` file with the Finnhub API Key credentials.

```
FINNUB_API_KEY=<FINNHUB_API_KEY>
```

3. Run `fastmcp install server.py` to install the server.

4. Open the configuration file located at:

   - On macOS: `~/Library/Application Support/Claude/claude_desktop_config.json`
   - On Windows: `%APPDATA%/Claude/claude_desktop_config.json`

5. Locate the command entry for `uv` and replace it with the absolute path to the `uv` executable. This ensures that the correct version of `uv` is used when starting the server.

6. Restart Claude Desktop to apply the changes.

## Development

Run `fastmcp dev server.py` to start the MCP server. MCP inspector is helpful for investigating and debugging locally.
