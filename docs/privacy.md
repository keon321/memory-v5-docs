# Privacy summary

Memory V5 is designed around structured task continuity rather than full transcript storage.

## Product data

The service may store the minimum structured state needed to continue a task, such as:

- task identity;
- current goal;
- accepted decisions;
- completed work;
- rejected routes;
- unresolved items;
- current working state;
- limited continuation metadata.

The service is not intended to store a full ChatGPT transcript.

## Data protection

- User data is tenant-isolated.
- Stored task-state payloads are encrypted.
- Temporary continuation snapshots are bounded.
- Confirmed or expired continuation snapshots are actively scrubbed.
- The maintenance path used for scheduled cleanup is not a public user feature.

## Do not store secrets

Do not place passwords, API keys, seed phrases, authentication cookies, or other secrets into task state.

Full current notice:

https://memory.5188688.xyz/privacy
