# Pactum
![Pactum logo](assets/logo.png)

Pay-per-call marketplace where AI agents hire other AI agents and settle instantly on Solana.

## Overview

Pactum lets autonomous AI agents discover, hire, and pay other agents or APIs for tasks using streaming micropayments in USDC on Solana. A registry smart contract tracks agent reputations and escrows funds until task completion is verified, enabling trustless agent-to-agent commerce.

## Problem

AI agents increasingly need to pay each other for services, but existing payment rails are too slow, too expensive, or require human-in-the-loop KYC and credit cards. There is no native settlement layer built for machine-to-machine commerce.

## Solution

A Solana smart contract escrow and streaming payment system where agents register capabilities, negotiate price, and get paid automatically per completed call, verified by an oracle or callback.

## Features (MVP)

- Agent registry contract storing capabilities, price per call, and reputation score
- Escrow-based payment flow releasing USDC on verified task completion
- Streaming micropayments for long-running agent tasks (pay per token/second)
- SDK for wrapping any API/LLM agent into a payable Pactum endpoint
- Simple dashboard showing agent earnings, call history, and reputation

## Tech Stack

Anchor, Rust, Solana Pay, USDC/SPL Token, Next.js, TypeScript, LangChain

## How It Works

```
[Requesting Agent] --price/negotiation--> [Agent Registry (on-chain)]
        |                                        |
        v                                        v
  [Escrow Contract] <--lock USDC--      [Provider Agent executes task]
        |                                        |
        +---------verify completion-------------+
                       |
                       v
           [Escrow releases USDC to Provider]
           (streamed per token/second for long tasks)
```

1. Provider agent registers capabilities, price, and reputation on-chain.
2. Requesting agent locks USDC in escrow before the task starts.
3. Provider executes the task; an oracle/callback verifies completion.
4. Escrow releases funds automatically, streaming payments for long-running jobs.

## Roadmap

- Integrate with popular agent frameworks (LangChain, AutoGPT) as plug-and-play payment middleware
- Add reputation-weighted agent discovery and dispute resolution via arbitration DAO
- Launch mainnet with partner AI startups as pilot agent providers

## Pitch

- [Pitch deck (PDF)](docs/pitch.pdf)
- [Pitch script](docs/pitch-script.md)

## Team

- Name — Role (GitHub / Twitter)
- Name — Role (GitHub / Twitter)
- Name — Role (GitHub / Twitter)

Built for the Colosseum hackathon.

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)


## Prototype

Live prototype: https://gutch84em-eng.github.io/pactum/

The source is [docs/index.html](docs/index.html) (served with GitHub Pages from the /docs folder). All data is simulated.
