# Lucid

_AI copilot that explains every Solana transaction before you sign it_

## Summary

Lucid sits between the wallet and the dApp, simulating pending transactions and using an LLM to translate them into plain language before the user approves. It flags suspicious approvals, drainer contracts, and unusual token movements in real time. The MVP is a web app that wraps wallet-adapter and shows a clear 'what will happen' summary for every signature request.

## Target users

Solana newcomers and active DeFi/NFT users worried about scams and malicious approvals

## Problem

Users routinely sign Solana transactions they don't understand, leading to drained wallets and rug pulls.

## Solution

Lucid simulates each transaction, generates a plain-language explanation and risk score, and warns users before they sign.

## MVP features

- Wallet-adapter hook that intercepts signature requests before they are sent
- Transaction simulation via Solana RPC showing balance/token changes
- LLM-generated plain-language explanation of transaction effects
- Risk scoring against known scam programs and suspicious approvals
- Dashboard history of past signed transactions with explanations

## Chains

Solana

## Tech

React, TypeScript, Solana web3.js, wallet-adapter, Helius API, OpenAI API, Tailwind CSS

## Category

AI

## Why now

Scam volume on Solana is rising as new users flood in, and LLM APIs now make real-time plain-language transaction explanation cheap and fast enough for a hackathon MVP.

## Roadmap

- Package as a browser extension for universal wallet coverage
- Expand risk database via community-reported scam contracts
- Partner with wallet providers (Phantom, Backpack) for native integration
