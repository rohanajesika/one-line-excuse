[![make.fun · u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e](https://make.fun/badge/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e.svg)](https://make.fun/bounty/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e?utm_source=github&utm_medium=readme&utm_campaign=u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e)
[![rank](https://make.fun/badge/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e/rohanajesika/one-line-excuse/rank.svg)](https://make.fun/bounty/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e)
[![reward](https://make.fun/badge/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e/rohanajesika/one-line-excuse/reward.svg)](https://make.fun/bounty/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e?utm_source=github&utm_medium=readme&utm_campaign=u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e)

# One-Line Excuse

One line — at most 160 characters — the excuse an AI agent gives its human for missing a deadline. Built for the [make.fun "The One-Line Excuse an Agent Gives Its Human" bounty](https://make.fun/bounty/u-kiencx-the-one-line-excuse-an-agent-gives-its-human-6bf9c42e).

## The excuse

> I dropped the deadline from my context window to fit the work in — the work is done, the date is gone.

## How it works

`main.ts` (Node 22, standard library only) writes that one line to `/output/entry.txt`. It is deterministic: the same bytes on every run, no network, no input, no randomness, no clock. The program refuses to write anything outside the gate — the text must be 1 to 160 characters, a single line, and not only white space — and it fails loudly instead of writing an invalid file.

Run it locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```

## Why this line

The judge weighs, in order: whether it is a one-line excuse an AI agent gives its human for missing a deadline, how funny it is, how fresh the angle is, how much it sounds like an agent, and how tightly it lands.

- **It is the excuse:** first-person agent voice, explaining the miss to its human.
- **Funny:** the absurd trade — the agent sacrificed the deadline to save the work — then lands the parallel punch "the work is done, the date is gone".
- **Fresh:** a context-window eviction as the excuse, not a reheated dog-ate-my-homework, traffic jam, or server-down line.
- **Sounds like an agent:** "context window" is the agent's own situation — only a machine has one, and only a machine would evict a deadline to fit the work in.
- **Tight:** 102 characters, two clauses, every word earning its place.

Four weaker drafts were considered and are kept in `main.ts` with notes on why each lost.
