# 🚀 Mempool MCP Server

A Model Context Protocol (MCP) server providing real-time Bitcoin blockchain and mempool data, powered by [mempool.space](https://mempool.space/) APIs. Use this server as a tool provider in your MCP-compatible clients (like Claude, Cursor, and others) to access up-to-date Bitcoin network information. Its an unofficial repository.

<a href="https://glama.ai/mcp/servers/@alexandresanlim/mempool-mcp-server">
  <img width="380" height="200" src="https://glama.ai/mcp/servers/@alexandresanlim/mempool-mcp-server/badge" alt="Mempool Server MCP server" />
</a>

---

## 🛠️ Available Bitcoin Tools

| Tool Name | Description |
|-----------|-------------|
| **get-difficulty-adjustment** | Get current and next Bitcoin difficulty adjustment info. |
| **get-price** | Get the current BTC price in various fiat currencies. |
| **get-historical-price** | Get the BTC price for a specific date (YYYY-MM-DD). |
| **get-recommended-fees** | Get recommended Bitcoin transaction fees. |
| **get-stats-info** | Get general Bitcoin network statistics. |
| **get-mining-pools** | Get mining pools info. |
| **get-mining-pool** | Get info for a specific mining pool. |
| **get-mining-blocks-fees-24h** | Get mining blocks fees for the last 24h. |
| **get-mempool-info** | Get mempool info. |
| **get-mempool-txids** | Get mempool txids. |
| **get-mempool-recent** | Get recent mempool transactions. |
| **get-blocks** | Get the latest blocks. |
| **get-block** | Get details about a block from its hash. |
| **get-block-txids** | Get txids for a block. |
| **get-block-txs** | Get transactions for a block. |
| **get-block-status** | Get block status. |
| **get-block-raw** | Get raw block hex. |
| **get-block-txid-by-index** | Get block txid by index. |
| **get-block-header** | Get the block header in hex. |
| **get-address-info** | Get details about an address. |
| **get-address-txs** | Get transactions for an address. |
| **get-address-txs-chain** | Get chain transactions for an address. |
| **get-address-txs-mempool** | Get mempool transactions for an address. |
| **get-address-utxo** | Get UTXOs for an address. |
| **get-tx-info** | Get details about a transaction. |
| **get-tx-status** | Get transaction status. |
| **get-tx-raw** | Get raw transaction hex. |
| **get-tx-merkleblock-proof** | Get transaction merkleblock proof. |
| **get-tx-outspend** | Get outspend info for a transaction output. |
| **get-tx-outspends** | Get outspends for all outputs of a transaction. |

---

## 🤖 What is MCP?

**Model Context Protocol (MCP)** is a standard for tool providers to communicate with AI clients via standard input/output. This server lets you plug Bitcoin data tools into any MCP-compatible client.

---

## ⚡ Quick Start: Use in Your MCP Client

You can configure this server as a tool provider in your MCP Client such Claude, Cursor, VsCode and others:

```json
"mempool-mcp-server": {
  "command": "npx",
  "args": [
    "@sanlim/mempool-mcp-server"
  ]
},
```

> [!TIP]
> To connect locally for privacy and unlimited calls, you can pass the base mempool API URL as an environment config from your local Bitcoin node such as Umbrel, MyNode, etc. See below:
> ```json
>"mempool-mcp-server-local": {
>  "command": "npx",
>  "args": [
>    "@sanlim/mempool-mcp-server"
>  ],
>  "env": {
>    "MEMPOOL_BASE_URL": "http://umbrel.local:3006/api"
>  }
>},
>```
> Check this working with "mempool url" text on your MCP Client.
> 
> <img src='https://github.com/alexandresanlim/mempool-mcp-server/blob/main/src/application/images/base_url_check.png?raw=true' width=600 />

Enjoy!

or

### 🛠️ Using a Local Build

1. **Clone this repository:**

```bash
git clone https://github.com/alexandresanlim/mempool-mcp-server.git
```

2. **Install and build:**

```bash
npm install
npm run build
npm run server
```

3. **Configure your MCP client:**

```json
"mempool-mcp-server-debug": {
  "command": "node",
  "args": [
    "...replace_to_path_of_project/mempool-mcp-server/build/main.js"
  ]
},
```

The server will start and listen for MCP requests via standard input/output. 🎉

---

## 📚 Reference & Troubleshooting

- Full API reference: [mempool.space API docs](https://mempool.space/docs/api/rest)
- If you have issues, make sure your build is up to date and your MCP client is configured to use stdio.
- For questions or contributions, feel free to open an issue or pull request!

---

Made with ❤️ by a bitcoiner. Enjoy!