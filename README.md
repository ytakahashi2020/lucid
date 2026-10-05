# Lucid
![Lucid logo](assets/logo.png)

**AI copilot that explains every Solana transaction before you sign it**

## Overview

Lucid is a web app that sits between your Solana wallet and any dApp. It simulates pending transactions and uses an LLM to translate them into plain language before you approve, flagging suspicious approvals, drainer contracts, and unusual token movements in real time.

## Problem

Users routinely sign Solana transactions they don't understand. Wallet popups show raw bytes and program instructions, not a clear description of what will actually happen. This leads to drained wallets, malicious approvals, and rug pulls, especially for newcomers.

## Solution

Lucid intercepts signature requests before they reach the wallet, simulates the transaction to compute real balance and token changes, generates a plain-language explanation with an LLM, and assigns a risk score so users can make an informed decision before signing.

## Features (MVP)

- Wallet-adapter hook that intercepts signature requests before they are sent
- Transaction simulation via Solana RPC showing balance/token changes
- LLM-generated plain-language explanation of transaction effects
- Risk scoring against known scam programs and suspicious approvals
- Dashboard history of past signed transactions with explanations

## Tech Stack

React, TypeScript, Solana web3.js, wallet-adapter, Helius API, OpenAI API, Tailwind CSS

## How It Works

```
  User Action            Lucid                         Result
------------------   ----------------------------   ------------------
dApp requests   -->  wallet-adapter hook             
signature            intercepts request
                      |
                      v
                 Solana RPC simulation (Helius)
                 -> balance & token changes
                      |
                      v
                 LLM (OpenAI) generates
                 plain-language summary
                      |
                      v
                 Risk scoring vs known
                 scam programs/approvals
                      |
                      v
                 "What will happen" screen  -->  User signs or rejects
                                                   in the wallet
```

## Roadmap

- Package as a browser extension for universal wallet coverage
- Expand risk database via community-reported scam contracts
- Partner with wallet providers (Phantom, Backpack) for native integration

## Pitch

- [Pitch deck (PDF)](docs/pitch.pdf)
- [Pitch script](docs/pitch-script.md)

## Team

- Name / role - contact
- Name / role - contact
- Name / role - contact

Built for the Colosseum hackathon.

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)
