ChainTrace: Open-Source AML Wallet Intelligence

https://img.shields.io/badge/version-1.0.0-blue.svg
https://img.shields.io/badge/License-MIT-yellow.svg
https://img.shields.io/badge/Chains-7_Supported-green.svg
https://img.shields.io/badge/Demo-Live_Now-success.svg

ChainTrace is a high-performance, open-source Anti-Money Laundering (AML) intelligence tool designed for Web3 security researchers, DAO delegates, and compliance analysts. Built to eliminate the high friction of enterprise compliance software, ChainTrace provides instant, no-KYC, zero-cost transaction tracing and risk scoring across 7 major blockchain networks.

· Live Demo: https://eklavyakumarsingh250-ctrl.github.io/chaintrace
· License: MIT
· Repository: GitHub – eklavyakumarsingh250-ctrl/chaintrace

---

Table of Contents

· Introduction
· The Problem
· The Solution
· Key Features
· Supported Blockchains
· How It Works
· Use Cases
· Getting Started
  · Live Tool
  · Local Development
· Technical Architecture
· Risk Scoring Methodology
· Data Sources and Integrations
· Privacy and Ethics
· Roadmap
· Contributing
· About the Architect
· License
· Disclaimer

---

Introduction

ChainTrace is an open-source intelligence (OSINT) platform tailored for the Web3 ecosystem. It empowers investigators to trace funds, detect money laundering patterns, and assess the risk of any wallet address across multiple blockchains—all without requiring an account, API key, or payment. By focusing on economic behavior rather than just smart contract code, ChainTrace bridges the gap between traditional AML compliance and the decentralized nature of blockchain finance.

---

The Problem

Decentralized Finance (DeFi) has unlocked unprecedented financial freedom, but it has also become a playground for malicious actors. Hacks, ransomware payments, and money laundering via mixers are daily occurrences. The tools to combat these threats are often:

· Expensive: Enterprise AML solutions cost thousands of dollars per month, placing them out of reach for independent researchers and small DAOs.
· Opaque: Proprietary scoring algorithms and black-box data sources make it difficult to verify results or understand why an address is flagged.
· Slow: Many compliance tools require lengthy onboarding, KYC checks, and manual report generation, delaying incident response.
· Centralized: They rely on private databases and are not auditable by the community.

As a result, security researchers, bug bounty hunters, and protocol delegates lack the immediate infrastructure to track stolen funds, map mixer hops, or verify safe counterparties. This information asymmetry allows illicit actors to operate with impunity.

---

The Solution

ChainTrace democratizes on-chain intelligence by providing a free, transparent, and real-time investigation terminal. With ChainTrace, any user can:

· Input a wallet address and instantly receive a comprehensive transaction history.
· Visualize the flow of funds through multiple hops, mixers, and exchanges.
· Obtain a dynamic risk score based on on-chain behavior and known threat databases.
· Generate exportable evidence reports for governance proposals, law enforcement, or internal audits.

ChainTrace is built on the philosophy of "Economic Risk Over Code Risk." While traditional audits focus on smart contract vulnerabilities, ChainTrace maps the economic logic of wallets to uncover systemic risks, such as "Whale Chokes" (concentrated liquidity that could destabilize a protocol) or connections to sanctioned addresses.

---

Key Features

ChainTrace offers a powerful yet intuitive interface for on-chain investigations:

· Multi-Chain Transaction Tracing
    Instantly map the full historical timeline of any target wallet address. Trace incoming and outgoing transactions across supported chains, with support for both EOAs (externally owned accounts) and contract addresses.
· Mixer and Tumbler Detection
    Algorithmic flagging of interactions with known privacy protocols (e.g., Tornado Cash, Railgun, Wasabi Wallet). The system identifies deposits and withdrawals from these mixers, highlighting potential money laundering activity.
· Counterparty Risk Flagging
    Cross-references addresses against databases of known illicit actors, including sanctions lists, hack victim addresses, and scam operations. Integrations with community-sourced data like ChainAbuse provide up-to-date threat intelligence.
· Dynamic Risk Scoring
    Generates a real-time risk score (0–100) based on multiple factors:
  · Direct or indirect contact with flagged addresses.
  · Usage of mixers or privacy tools.
  · Transaction velocity and patterns.
  · Age of the wallet and balance thresholds.
      The scoring model is transparent and continuously improved through community feedback.
· Exportable Evidence Reports
    One-click generation of PDF or CSV reports summarizing the investigation. Reports include transaction graphs, risk scores, and flagged interactions—perfect for DAO governance submissions, bug bounty evidence, or law enforcement handover.
· No KYC, No Cost, No Limits
    ChainTrace is completely free and open-source. No registration, no API keys, and no rate limiting for basic queries. Advanced users can run their own instance or contribute to the data sources.

---

Supported Blockchains

ChainTrace currently supports cross-chain intelligence on the following networks (v1.0):

· Ethereum (ETH) – Mainnet and all major testnets
· Arbitrum (ARB) – One and Nova
· Binance Smart Chain (BSC) – Mainnet
· Polygon (MATIC) – PoS mainnet
· Solana (SOL) – Mainnet
· Bitcoin (BTC) – Mainnet
· TRON (TRX) – Mainnet

Support for additional chains (Avalanche, Optimism, Base, etc.) is planned for future releases.

---

How It Works

ChainTrace operates as a lightweight web application that queries public blockchain data through various RPC endpoints and APIs. The workflow is straightforward:

1. Address Input – The user selects a network and enters a wallet address or transaction hash.
2. Data Aggregation – ChainTrace fetches transaction history from the respective blockchain RPC, supplemented by data from block explorers and threat intelligence APIs.
3. Graph Construction – Transactions are processed to build a directed graph of fund flows, identifying patterns such as circular flows, high-frequency transfers, and mixer interactions.
4. Risk Analysis – The risk engine evaluates the address based on predefined rules and heuristic models, producing a risk score and detailed flags.
5. Visualization – Results are displayed in a clean terminal-like interface, with collapsible sections for transactions, flags, and summary metrics.
6. Export – Users can download the report for further analysis or sharing.

All processing happens client-side whenever possible to preserve privacy; only necessary blockchain queries are sent to public nodes or proxies.

---

Use Cases

ChainTrace serves a wide range of Web3 participants:

· Security Researchers & Bug Bounty Hunters
    Quickly assess whether a reported vulnerability has been exploited, trace stolen funds, and provide actionable evidence to protocols.
· DAO Delegates & Governance Participants
    Vet treasury proposals by examining the counterparties involved and ensuring no funds flow from risky addresses.
· Compliance Analysts
    Perform due diligence on potential partners, verify the legitimacy of large transactions, and generate reports for regulatory submissions.
· DeFi Protocols
    Monitor whale wallets for unusual behavior that could signal market manipulation or impending liquidation cascades.
· Law Enforcement & Regulators
    Access a free, transparent tool to aid in investigations without being locked into expensive vendor contracts.
· Individual Users
    Verify the safety of an address before interacting with it, or understand the history of a wallet you’re considering transacting with.

---

Getting Started

Live Tool

You can start using ChainTrace immediately without any setup:

1. Visit the live terminal: https://eklavyakumarsingh250-ctrl.github.io/chaintrace
2. Select the target network from the dropdown (e.g., Arbitrum).
3. Enter a wallet address or transaction hash.
4. Click TRACE -> to generate the intelligence report.

The interface is designed for both desktop and mobile browsers.

Local Development

If you wish to run ChainTrace locally or contribute to development:

```bash
# Clone the repository
git clone https://github.com/eklavyakumarsingh250-ctrl/chaintrace.git
cd chaintrace

# Install dependencies (if any; the project may be static HTML/JS)
# For a typical static site, you can simply open index.html in a browser.

# For a more advanced setup with Node.js:
npm install
npm start
```

Refer to the repository's README for detailed build instructions.

---

Technical Architecture

ChainTrace is built with a modular, open architecture:

· Frontend – Pure HTML, CSS, and JavaScript (no heavy frameworks) for maximum accessibility and easy self-hosting. The terminal-style UI is responsive and lightweight.
· Blockchain Data Layer – Queries are made to public RPC endpoints (e.g., Infura, Alchemy, public nodes) and block explorer APIs (Etherscan, BscScan, etc.). All queries are anonymized where possible.
· Risk Engine – A client-side JavaScript module applies heuristic rules to transaction data. Rules are stored in a JSON format and can be updated via community contributions.
· Threat Intelligence Feeds – Integration with open databases like ChainAbuse, Etherscan's address tags, and manually curated lists of high-risk addresses.
· Export Module – Generates reports using browser APIs (PDF via html2canvas + jsPDF, CSV via blob download).

The architecture prioritizes transparency: every rule and data source is auditable in the repository.

---

Risk Scoring Methodology

The risk score is a composite metric designed to reflect the likelihood that an address is involved in illicit activity. It is calculated based on the following weighted categories:

Category Weight Description
Direct Sanctions Match 40% Address appears on OFAC or other sanctions lists.
Mixer Interaction 25% Address has deposited to or withdrawn from known mixers.
Indirect Exposure 15% Transactions with addresses that themselves have high-risk scores (two hops).
Transaction Velocity 10% Unusually high frequency or volume of transactions suggestive of layering.
Wallet Age & Activity 5% Very new wallets with high-value transfers are riskier.
Community Reports 5% Reports from platforms like ChainAbuse (with verification).

The final score is normalized to a 0–100 scale. A score above 70 indicates high risk and warrants further investigation.

Note: The scoring model is heuristic and may produce false positives. Always verify flags manually.

---

Data Sources and Integrations

ChainTrace aggregates data from multiple public sources to maximize coverage:

· Blockchain RPCs – Direct on-chain data for Ethereum, BSC, Polygon, Arbitrum, Solana, Bitcoin, and TRON.
· Block Explorers – Supplemental APIs for transaction decoding and internal transactions (e.g., Etherscan, BscScan, Tronscan).
· Threat Intelligence Feeds
  · ChainAbuse – Community-reported scam and abuse addresses.
  · OFAC Sanctions List – Specially Designated Nationals (SDN) list.
  · Etherscan Labels – Publicly tagged addresses.
  · Manual curation by the ChainTrace community.
· Mixer Registries – A continuously updated list of known mixer contracts and their associated addresses.

All data sources are publicly accessible; no proprietary databases are used.

---

Privacy and Ethics

ChainTrace is designed with privacy and ethical use in mind:

· No Tracking – The live tool does not collect or store user IP addresses or search queries. All analysis happens client-side; no data is sent to a backend server except necessary blockchain RPC calls.
· Transparency – Every rule and data source is open for review. Users can verify why an address was flagged.
· Ethical Use – ChainTrace is intended for legitimate research, compliance, and security purposes. Misuse for harassment or illegal activities is strictly prohibited.

We encourage responsible disclosure of any vulnerabilities found using ChainTrace.

---

Roadmap

Future development plans include:

· Q3 2024: Support for additional chains (Avalanche C-Chain, Optimism, Base).
· Q4 2024: Integration with NFT transaction tracing and ERC-20 token flows.
· Q1 2025: Machine learning-based anomaly detection for identifying new mixer patterns.
· Q2 2025: API access for programmatic queries (rate-limited free tier).
· Ongoing: Community-driven expansion of threat intelligence feeds and risk scoring rules.

We welcome community input on priorities. Please open an issue or discussion on GitHub.

---

Contributing

ChainTrace thrives on community contributions. Whether you're a developer, security researcher, or data analyst, you can help:

· Report False Positives/Negatives – Open an issue with details.
· Add New Mixer Addresses – Submit a pull request to update mixers.json.
· Improve Risk Scoring – Propose new heuristics or weights.
· Translate UI – Help localize the interface.
· Documentation – Improve this README or add tutorials.

Please read our Contributing Guidelines before submitting a pull request.

---

About the Architect

Eklavya (Project Sentinel) is a lead independent security researcher specializing in Economic Incident Response (IR) and Logic Collisions. With a background as a veteran trader, Eklavya focuses on bridging the gap between L2 core security and dApp-layer economic risk. Current initiatives include proposing standardized "Economic IR Playbooks" for the Arbitrum DAO (DDA 3.0) and building open-source tools to empower the community.

· GitHub: @eklavyakumarsingh250-ctrl
· Twitter: @EklavyaOnChain (placeholder)

---

License

ChainTrace is open-source software licensed under the MIT License. You are free to use, modify, and distribute it, subject to the terms of the license.

---

Disclaimer

ChainTrace is an intelligence tool provided for research and educational purposes only. It does not constitute legal or financial advice. The risk scores and flags are based on heuristic models and public data; they may not be accurate or complete. Always conduct your own due diligence before making any decisions based on the output of this tool. The authors and contributors assume no liability for any actions taken or not taken based on the information provided.
