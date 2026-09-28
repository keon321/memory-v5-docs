# Memory V5

**Switch chats. Keep the project.**

Memory V5 helps people continue long-running ChatGPT work in a new chat without re-explaining the whole project.

It is designed for work that spans days or weeks: coding, research, product work, writing, learning, and other long-running tasks where losing decisions or progress is expensive.

## The problem

Long chats eventually become slow, hit context limits, or become hard to steer. A normal summary often loses exactly the things that matter most:

- what the real goal is;
- which decisions are already settled;
- what has been completed;
- which approaches were rejected;
- what is still unresolved;
- what should happen next.

Memory V5 stores structured task state instead of trying to preserve the entire transcript.

## How it works

1. Save the current task state.
2. Open a new ChatGPT chat.
3. Paste the continuation package.
4. Review the recovered state.
5. Confirm it, then continue the original work.

The new chat does not silently guess which task you meant. If identity is uncertain, the system should stop instead of restoring the wrong task.

## Public free test

Memory V5 is currently in a public free-test stage.

The free tier includes:

- 3 active tasks;
- structured task-state saving;
- exact continuation into a new chat;
- user confirmation before the recovered state becomes canonical;
- export of current task state;
- confirmed deletion.

The core continuation experience is not intentionally degraded for free users.

Future paid features are expected to focus on scale and management: more active tasks, version history, restore, archive, search, and advanced project views. Pricing has not been announced.

## Start

**Start free:** https://memory-v5-beta.8084867.workers.dev/start

Product page: https://memory-v5-beta.8084867.workers.dev/

Pricing/status: https://memory-v5-beta.8084867.workers.dev/pricing

## What Memory V5 is not

- Not a full transcript backup.
- Not a replacement for your own backups of important files.
- Not a secret vault.
- Not a promise that every model response is a verified fact.
- Not an excuse to guess task identity from similar titles.

## Privacy

The service stores the minimum structured state needed for task continuation rather than a full chat transcript.

Task state is tenant-isolated and encrypted in the service. Temporary continuation snapshots are bounded and are actively scrubbed after expiry or confirmation.

Do not put passwords, API keys, seed phrases, or other secrets into task state.

More detail: https://memory-v5-beta.8084867.workers.dev/privacy

## Feedback

This repository is the public product/documentation and feedback surface for Memory V5.

The core service repository remains private. This repository is not a source-code release.

Please use GitHub Issues for:

- recovery omissions;
- confusing onboarding;
- documentation errors;
- reproducible product bugs;
- feature requests that come from real usage.

For a recovery problem, please describe the symptom without pasting private task content or continuation tokens.

## Current scope

The first public surface is ChatGPT Web.

The longer-term product direction is model-neutral continuity: the task should remain coherent even when the chat changes and, eventually, when the AI host changes.

---

[中文说明](README.zh-CN.md)
