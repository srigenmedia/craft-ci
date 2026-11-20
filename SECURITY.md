# Security Policy

## Fail-Closed Guarantees

1. **Zero Secret Echo:** CraftCI never echoes raw API keys, tokens, or credentials in audit reports or MCP responses.
2. **Server-Authoritative Billing:** B2B SaaS plans are validated strictly against frozen server SKU catalogs (`SAC_998315` INR 18% GST via Razorpay; `EXPORT_LUT_0PCT` USD via PayPal) with constant-time HMAC-SHA256 verification and replay deduplication.
3. **Zero-Custody Safe-Harbor:** Holds `₹0.00` customer funds.
4. **Fail-Closed AuthN & BOLA:** Protected `/mcp` (`tools/call`) and `/api/v1/billing/report` endpoints enforce `HTTP 401` and `HTTP 403` tenant isolation.

## Reporting a Vulnerability

Email `security@srigenmedia.com` with reproduction details.
