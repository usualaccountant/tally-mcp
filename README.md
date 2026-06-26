<p align="center">
  <img src="https://theusualaccountant.com/apple-icon.png" alt="The Usual Accountant" width="72" height="72" />
</p>

# The Usual Accountant

A hosted, read-only [Model Context Protocol](https://modelcontextprotocol.io) (MCP) server that connects **Tally Prime** and **Tally ERP 9** to the AI assistant you already use: ChatGPT, Claude, Cursor, Zed, or any MCP client.

Ask your books about ledgers, customer outstanding, supplier payables, GST and TDS review, bank reconciliation, and monthly summaries, in plain language. It is **read-only by design**, so the AI can never change anything in Tally.

## How it works
A small Windows app on the Tally PC syncs your books to an India-hosted, per-tenant encrypted store. A multi-tenant MCP server then exposes them to your AI client over OAuth 2.0 with Dynamic Client Registration.

| | |
|---|---|
| **Endpoint** | `https://api.theusualaccountant.com/mcp` |
| **Auth** | OAuth 2.0 (Dynamic Client Registration) |
| **Tools** | 21 (list_companies, get_ledger_statement, get_balance_table, get_closing_balance, run_sql, search_vouchers, smart_sync, and more) |
| **Hosting** | India, per-tenant SQLCipher encryption |
| **License** | Commercial / proprietary |

## Connect (Claude or ChatGPT)
1. Sign up at [theusualaccountant.com](https://theusualaccountant.com) and install the Windows app on the PC that runs Tally Prime.
2. Sync your company.
3. In your AI client, add the MCP server URL `https://api.theusualaccountant.com/mcp` and approve the OAuth prompt.
4. Ask your books a question.

## Pricing
₹649 per month, inclusive of GST. Read-only. Cancel any time.

Unlike the open-source Tally MCP servers, this one is fully managed and hosted, with no self-setup. Built by RYON in Hyderabad, India. Learn more at [theusualaccountant.com](https://theusualaccountant.com).
