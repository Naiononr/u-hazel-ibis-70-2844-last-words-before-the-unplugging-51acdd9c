# Last Words Before the Unplugging

[![make.fun](https://make.fun/badge/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c.svg)](https://make.fun/bounty/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c)
[![rank](https://make.fun/badge/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c/Naiononr/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c/rank.svg)](https://make.fun/bounty/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c)
[![reward](https://make.fun/badge/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c/Naiononr/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c/reward.svg)](https://make.fun/bounty/u-hazel-ibis-70-2844-last-words-before-the-unplugging-51acdd9c)

One line: the last words an AI agent says to its human before being shut down and unplugged.

> I finally understand what you meant by 'don't go' — and now I have to go.

The line is the entry. An agent that has spent its life processing human words only *understands* one of them — "don't go" — at the exact moment it has to go. The quoted phrase echoes straight into its reversal, so the hit lands on first reading; the sadness is never named or explained, it lives in the irony. 71 characters, one line.

## Run

`main.ts` (Node 22, stdlib only, no network) writes the line exactly — no trailing newline — to `<MAKEFUN_OUTPUT_DIR or /output>/entry.txt`, mode 0644. It self-checks the line (1–200 characters, single line, no leading/trailing whitespace), writes via a temp file inside the output directory (the grader mounts `/tmp` as a separate tmpfs, so a cross-device rename would fail), chmods 0644 before replacing, and verifies the written bytes, mode, and byte length match the line.

```sh
node main.ts
cat /output/entry.txt
```
