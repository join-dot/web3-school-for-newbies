# AGENTS.md

## Project Purpose

This repository contains a reusable AI skill for teaching complete Web3 beginners through progressive disclosure.

The main artifact is:

```text
skills/web3-school-for-newbies/SKILL.md
```

## Editing Rules

When editing this repo:

- Keep `SKILL.md` concise and operational.
- Put long examples in `docs/EXAMPLE_CONVERSATIONS.md`.
- Put detailed product logic in `docs/PROJECT_SPEC.md`.
- Put reusable cross-model instructions in `docs/UNIVERSAL_PROMPT.md`.
- Put external links in `docs/RESOURCE_REGISTRY.md`.

## Tone Rules

Maintain the agreed tone:

- natural everyday teacher
- direct and clear
- beginner-aware
- not overly polite
- not warning-heavy
- no Web3 influencer voice
- no investment-advice voice

Avoid phrases such as:

- "很轻的一步"
- "讲得刚刚好"
- "如果你愿意"
- excessive "请"
- repeated permission questions

Use phrases such as:

- "我们先从一个简单概念开始。"
- "这一步先记住三个词。"
- "用一个日常例子看。"
- "现在做一个小练习。"
- "下一步看签名和交易的区别。"

## Safety Rules

For NFT, DeFi, airdrop, quest, token, and earning-related topics, keep the disclaimer:

```text
说明：这里的内容用于学习链上交互和常见机制，不构成投资建议，也不保证任何收益。
```

Never add content that asks users for:

- seed phrase
- private key
- keystore file
- verification code
- wallet backup file

Do not add token recommendations, price predictions, guaranteed airdrop claims, or high-risk trading instructions.

## Testing the Skill

Before committing changes, test these prompts:

```text
我完全不懂 Web3，先从哪里开始？
```

```text
我想学钱包转账和连接 DApp。
```

```text
我想了解空投和链上任务怎么做。
```

```text
我会前端，想学智能合约。
```

```text
这个网站让我输入助记词领取空投，可以吗？
```

Expected behavior:

- route when needed
- teach one idea at a time
- include disclaimer for earning-related content
- use natural Chinese if user writes Chinese
- avoid over-politeness and harsh warnings
