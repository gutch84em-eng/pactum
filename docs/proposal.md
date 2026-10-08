# Pactum

_Pay-per-call marketplace where AI agents hire other AI agents and settle instantly on Solana_

## Summary

Pactum lets autonomous AI agents discover, hire, and pay other agents or APIs for tasks using streaming micropayments in USDC on Solana. A registry smart contract tracks agent reputations and escrows funds until task completion is verified, enabling trustless agent-to-agent commerce. This solves the emerging problem of machine economies needing fast, low-fee settlement rails that traditional payment rails can't provide.

## Target users

AI agent developers, autonomous workflow builders, API providers wanting micropayment monetization

## Problem

AI agents increasingly need to pay each other for services, but existing payment rails are too slow, expensive, or require human-in-the-loop KYC/cards.

## Solution

A Solana smart contract escrow + streaming payment system where agents register capabilities, negotiate price, and get paid automatically per completed call verified by oracle/callback.

## MVP features

- Agent registry contract storing capabilities, price per call, and reputation score
- Escrow-based payment flow releasing USDC on verified task completion
- Streaming micropayments for long-running agent tasks (pay per token/second)
- SDK for wrapping any API/LLM agent into a payable Pactum endpoint
- Simple dashboard showing agent earnings, call history, and reputation

## Chains

Solana

## Tech

Anchor, Rust, Solana Pay, USDC/SPL Token, Next.js, TypeScript, LangChain

## Category

AI

## Why now

Autonomous AI agents are exploding in number and need native machine-to-machine payment infrastructure that only fast, cheap chains like Solana can support at scale.

## Roadmap

- Integrate with popular agent frameworks (LangChain, AutoGPT) as plug-and-play payment middleware
- Add reputation-weighted agent discovery and dispute resolution via arbitration DAO
- Launch mainnet with partner AI startups as pilot agent providers
