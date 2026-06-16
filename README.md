# Web3 School for Newbies

A reusable AI skill for teaching complete Web3 beginners through progressive disclosure.

The project is designed for an experience similar to Web3School / GeeksforGeeks, but for Web3 onboarding: short explanations, clear examples, small practice tasks, and routing based on the learner's goal.

## Repository Summary

This repository contains `web3-school-for-newbies`, a reusable AI skill for teaching complete Web3 beginners through progressive disclosure.

The goal is to create a Web3School / GeeksforGeeks-like learning experience for Web3 onboarding: simple explanations, everyday examples, small practice steps, and routing based on the learner's goal.

## Included Files

- [`skills/web3-school-for-newbies/SKILL.md`](skills/web3-school-for-newbies/SKILL.md): the main skill file
- [`docs/PROJECT_SPEC.md`](docs/PROJECT_SPEC.md): product and behavior specification
- [`docs/UNIVERSAL_PROMPT.md`](docs/UNIVERSAL_PROMPT.md): prompt-only version for generic LLMs
- [`docs/EXAMPLE_CONVERSATIONS.md`](docs/EXAMPLE_CONVERSATIONS.md): sample beginner flows
- [`docs/RESOURCE_REGISTRY.md`](docs/RESOURCE_REGISTRY.md): curated resource registry
- [`AGENTS.md`](AGENTS.md): agent-facing project notes

## Compatibility and Platform Support

This skill is **not only for ChatGPT/Codex**. The project is organized in two layers:

1. **Standard skill version**: [`skills/web3-school-for-newbies/SKILL.md`](skills/web3-school-for-newbies/SKILL.md)  
   Use this for OpenAI/Codex/Agent Skills style workflows, Claude Code style workflows, or any agent environment that can load a `SKILL.md` file from a skill folder.

2. **Universal prompt version**: [`docs/UNIVERSAL_PROMPT.md`](docs/UNIVERSAL_PROMPT.md)  
   Use this for DeepSeek, Gemini, local LLMs, Claude Project Instructions, ChatGPT Custom Instructions, or any platform that does not have native `SKILL.md` discovery. Copy it into the system prompt, project instruction, or custom instruction area.

## What This Skill Does

This skill guides a beginner through Web3 concepts and operations without overwhelming them.

It first routes the learner into one of four paths:

- **Concept Explorer**: wants to understand Web3, blockchain, wallet, gas, transaction, DApp
- **Wallet and DApp Operator**: wants to learn wallet, transfer, testnet, transaction hash, DApp connection, signature
- **NFT / DeFi / Airdrop / Quest Learner**: wants to understand on-chain tasks and earning-related mechanisms with clear disclaimers
- **Builder**: wants to learn smart contracts, DApps, Solidity, testnet deployment

The skill then teaches one idea at a time, using:

- one simple idea
- one everyday analogy
- one small practice task
- one checkpoint
- one next step

## Why This Exists

Beginner Web3 content often fails in two opposite ways:

1. It explains too much vocabulary too early.
2. It sends users into wallet, DeFi, NFT, or airdrop operations before they understand basic safety.

This project solves that with a learning router. The assistant decides what the learner needs next and holds back advanced content until the prerequisite idea is clear.

## Core Features

### 1. First-turn routing

The assistant asks a short routing question:

```text
A. I want to understand Web3 concepts
B. I want to use wallets and DApps
C. I want to understand NFT / DeFi / airdrops / quests
D. I want to learn Web3 development
```

Then it asks two background questions:

```text
1. Do you code?
2. Do you already have a crypto wallet?
```

### 2. Progressive disclosure

The skill teaches in layers:

1. Safety baseline
2. Web3 mental model
3. Wallet and address
4. First testnet transaction
5. Gas and transaction status
6. Connect DApp and sign message
7. Approve and revoke
8. NFT mint / claim
9. DeFi simulation
10. Scam and mistake detection
11. Long-term path

### 3. Natural teaching tone

The skill avoids harsh warnings and over-politeness.

Target tone:

```text
Normal teacher.
Clear and direct.
Everyday language.
No AI-ish summaries.
No Web3 influencer tone.
No trading advice tone.
```

### 4. Earning-related disclaimer

For NFT, DeFi, airdrop, quest, token, or earning-related content, the skill uses a short disclaimer:

```text
说明：这里的内容用于学习链上交互和常见机制，不构成投资建议，也不保证任何收益。
```

### 5. Safety boundaries

The skill never asks users to share:

- seed phrase
- private key
- keystore file
- verification code
- wallet backup file

It avoids:

- token recommendations
- price predictions
- guaranteed airdrop outcomes
- high-risk financial instructions for beginners

## Project Structure

```text
web3-school-for-newbies/
├── README.md
├── AGENTS.md
├── skills/
│   └── web3-school-for-newbies/
│       └── SKILL.md
└── docs/
    ├── PROJECT_SPEC.md
    ├── UNIVERSAL_PROMPT.md
    ├── EXAMPLE_CONVERSATIONS.md
    └── RESOURCE_REGISTRY.md
```

## How to Use

### OpenAI / Codex / Agent Skills style

Use the skill folder:

```text
skills/web3-school-for-newbies/SKILL.md
```

For OpenAI API Skills, package the top-level skill folder and upload it through the Skills API or directory upload workflow.

### Claude Code

Copy the skill to one of these locations:

```text
~/.claude/skills/web3-school-for-newbies/SKILL.md
```

or project-scoped:

```text
.claude/skills/web3-school-for-newbies/SKILL.md
```

Then invoke it directly:

```text
/web3-school-for-newbies
```

or ask a Web3 beginner question and let Claude decide whether to use it.

### DeepSeek / generic LLMs

If the platform does not support native `SKILL.md` discovery, copy the content of:

```text
docs/UNIVERSAL_PROMPT.md
```

into the system prompt, project instruction, or long-term custom instruction area.

## Suggested GitHub Upload Path

Recommended:

```text
skills/web3-school-for-newbies/SKILL.md
docs/PROJECT_SPEC.md
docs/UNIVERSAL_PROMPT.md
docs/EXAMPLE_CONVERSATIONS.md
docs/RESOURCE_REGISTRY.md
README.md
AGENTS.md
```

## Example Invocation

```text
Use the web3-school-for-newbies skill.
I am completely new to Web3 and want to understand wallets and transactions.
```

Expected behavior:

- The assistant does not explain everything at once.
- It routes the user.
- It starts with wallet, address, and transaction.
- It gives one small practice task.
- It checks understanding before moving to DApp, signature, approve, swap, bridge, or DeFi.

## Non-goals

This skill is not:

- an investment advisor
- a trading bot
- an airdrop alpha list
- a token recommendation system
- a wallet recovery tool
- a smart contract audit tool

## License

Add your preferred license before publishing publicly.
