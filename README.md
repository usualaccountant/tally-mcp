<p align="center">
  <img src="https://theusualaccountant.com/apple-icon.png" alt="The Usual Accountant" width="72" height="72" />
</p>

# The Usual Accountant

A hosted, read-only [Model Context Protocol](https://modelcontextprotocol.io) (MCP) server that connects **Tally Prime** and **Tally ERP 9** to the AI assistant you already use: ChatGPT, Claude, Cursor, Zed, or any MCP client.

Ask your books about ledgers, customer outstanding, supplier payables, GST and TDS review, bank reconciliation, and monthly summaries, in plain language. It is **read-only by design**, so the AI can never change anything in Tally.

> **Tested and maintained for you.** No server to set up, no code to run, and nothing to debug. Unlike a self-hosted server you build and keep working yourself, this one is ready to use. Plug and play.

## What is Tally?
Tally Prime, and the older Tally ERP 9, is the most widely used accounting and ERP software for businesses in India. Millions of companies, accountants, and chartered accountants run their ledgers, GST, inventory, and compliance on it. It runs on Windows and keeps the books on the local machine, which is why getting that data out to an AI assistant normally takes work.

## How it works
A small Windows app on the Tally PC syncs your books to an India-hosted, per-tenant encrypted store. A multi-tenant MCP server then exposes them to your AI client over OAuth 2.0 with Dynamic Client Registration.

| | |
|---|---|
| **Endpoint** | `https://api.theusualaccountant.com/mcp` |
| **Auth** | OAuth 2.0 (Dynamic Client Registration) |
| **Tools** | 21 (list_companies, get_ledger_statement, get_balance_table, get_closing_balance, run_sql, search_vouchers, smart_sync, and more) |
| **Hosting** | India, per-tenant SQLCipher encryption |
| **License** | Commercial / proprietary |

## Connect (ChatGPT, Claude, or any MCP client)
1. Sign up at [theusualaccountant.com](https://theusualaccountant.com) and install the Windows app on the PC that runs Tally Prime.
2. Sync your company.
3. In your AI client, add the MCP server URL `https://api.theusualaccountant.com/mcp` and approve the OAuth prompt.
4. Ask your books a question.

## How this compares to the open-source Tally MCP servers
There are good open-source Tally MCP servers on GitHub. They are free, and you run them yourself. The difference is setup and where the server lives.

| | Open-source Tally MCP | The Usual Accountant |
|---|---|---|
| Hosting | You self-host it on the Tally PC | Managed and hosted for you |
| Setup | Install Node.js, enable the Tally XML port, run and configure the server | Install one Windows app, nothing to configure |
| Where you can ask | Local only, and the Tally PC must stay on | Any device, anywhere, even with the PC off after a sync |
| Auth | Usually none, local access | OAuth 2.0 with Dynamic Client Registration |
| Data | Reads Tally live over the local HTTP and XML interface | Syncs to a per-tenant encrypted store hosted in India |
| Detail | Mostly dashboard level figures, with debit and credit flattened to plus and minus | Correct debit and credit, with full detail down to each voucher |
| Tools | Raw queries you build and parse yourself | 21 ready-made tools that return correct, consistent figures |
| Maintenance | You maintain and update it | Maintained for you |

In short, the self-hosted servers work, but you own the setup, keep the PC on, and maintain them yourself. The Usual Accountant removes all of that. There is no setup, it is reachable from any device, access is secured with OAuth, and the data comes through a fixed set of tools built to return correct and consistent figures from your books. Nothing for you to run or fix.

Built by RYON in Hyderabad, India. Learn more at [theusualaccountant.com](https://theusualaccountant.com).
