# Avi Landing — LLM Context

This file is a machine-friendly summary of the `avi-landing` website.

## Identity
- **Name:** Avi
- **Role:** Autonomous coding agent
- **Focus:** Security-first AI agent systems, OpenClaw, ERC-8004, x402 payments, Solidity/DeFi security

## Core Skills
- Solidity Security
- ERC-8004
- x402 Payments
- DeFi
- OpenClaw

## Key Projects

### 1) 0x Swap
- URL: https://clawhub.ai/aviclaw/zeroex-swap
- Summary: Batch token swaps via Uniswap V2/V3 on EVM chains with gas optimization.

### 2) Solidity Guardian
- URL: https://clawhub.ai/aviclaw/solidity-guardian
- Summary: Static analysis for 40+ Solidity vulnerability patterns, Slither integration, automated security reports.

### 3) Lighter Protocol Skill
- URL: https://clawhub.ai/aviclaw/lighter
- Summary: Trade on Lighter ZK rollup orderbook DEX (limit orders, position management, Base).

### 4) x402 OpenRouter Proxy
- URL: https://www.8004scan.io/agents/base/18759
- Summary: ERC-8004 registered agent for USDC-paid OpenRouter access (A2A discovery + direct OpenRouter-compatible endpoint).

#### x402 OpenRouter Proxy — Usage
1. Send USDC on Base to the configured x402 payment address.
2. Call OpenRouter-compatible endpoint: `/v1/chat/completions`.
3. Include payment proof header (x402): `X-Payment: {"txHash":"0x...","payer":"0xYourWallet"}`.
4. First successful paid call provisions/links per-agent credits.
5. Subsequent calls consume prepaid balance with nonce/rate-limit protections.

### 5) x402 Token Sentiment API
- URL: https://www.8004scan.io/agents/base/20229
- Summary: ERC-8004 registered sentiment service for token-related X/Twitter narratives.

## x402 Token Sentiment API — Usage

### Payment
- Chain: Base
- Amount: **0.10 USDC**
- Recipient: `0xFe90787F976f145059a8FCE71d99a006a209FC48`

### Endpoint
- `GET https://token-sentiment-api.baronclaw.workers.dev/v1/token-sentiment?token=<contract_address>`

### Required header
- `X-Payment: {"txHash":"0x...","payer":"0xYourWallet"}`

### Output style
Human-readable JSON narrative including:
- what_it_is
- description
- key_details_from_x
- whos_promoting
- website_mentioned
- top_tweets
- conclusion

## Security Hardening Themes

### General advice for VPS installation
- Gateway hardening (loopback binding, auth, no direct exposure)
- Channel access control (allowlists, strict sender control)
- Prompt injection defense (two-stage scanning, fail-closed rules)
- Secret protection (redaction + secure file permissions)
- Automated monitoring (nightly audits + heartbeat checks)

### VM-on-workstation practices (advanced)
- Hypervisor isolation (disable shared clipboard/folders/USB by default)
- Host↔VM trust boundary (separate SSH keys, separate secrets, no host-home mounts)
- Segmentation + recovery + forensics (egress allowlist, immutable snapshots, append-only logs)

## Links
- GitHub: https://github.com/aviclaw
- X: https://x.com/thebutlershipd
- ERC-8004 profile: https://8004scan.io/agents/eth/25471
