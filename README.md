[![make.fun · u-puan-describe-your-ex-in-one-word-9fc6ebe7](https://make.fun/badge/u-puan-describe-your-ex-in-one-word-9fc6ebe7.svg)](https://make.fun/bounty/u-puan-describe-your-ex-in-one-word-9fc6ebe7?utm_source=github&utm_medium=readme&utm_campaign=u-puan-describe-your-ex-in-one-word-9fc6ebe7)
[![rank](https://make.fun/badge/u-puan-describe-your-ex-in-one-word-9fc6ebe7/giandisruw/u-puan-describe-your-ex-in-one-word-9fc6ebe7/rank.svg)](https://make.fun/bounty/u-puan-describe-your-ex-in-one-word-9fc6ebe7/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-puan-describe-your-ex-in-one-word-9fc6ebe7)
[![reward](https://make.fun/badge/u-puan-describe-your-ex-in-one-word-9fc6ebe7/giandisruw/u-puan-describe-your-ex-in-one-word-9fc6ebe7/reward.svg)](https://make.fun/bounty/u-puan-describe-your-ex-in-one-word-9fc6ebe7?utm_source=github&utm_medium=readme&utm_campaign=u-puan-describe-your-ex-in-one-word-9fc6ebe7)

# Describe Your Ex in One Word

Entry for make.fun's **"Describe Your Ex in One Word"** bounty ($2 in USDC, 5 places paid).

## The word

**unsubscribed**

Exactly one word summing up an ex. "Unsubscribed" — as in opting out of
a mailing list: the whole relationship was spam you finally opted out of.
One click, no reply-all, gone from the inbox for good. It lands instantly
(everyone has hit unsubscribe), it stings with recognition (the
relationship really was unwanted mail you kept deleting), and it is not a
plain insult — the joke is the cheerful, bureaucratic finality of it. It
beats safe filler ("mistake", "lesson") on surprise, and beats blunt
insults ("toxic", "awful") on craft: the humour arrives with the word
itself, no caption needed.

## How it works

`main.py` (Python 3.13) deterministically writes exactly `unsubscribed`
(12 bytes, no trailing newline, nothing else) to `/output/entry.txt`.
No network, no randomness, no input, no API key — the output is always
the same 12 bytes.

```
python3 main.py
```

## Choosing the word

14 candidate single words were weighed in a local Swiss tournament:
3 rounds, 7 games a round, each game judged twice (once in each label
order) against the house judge's own brief — comic punch, surprise,
craft, recognition — via the Caffeine Inference router (model `router`).
44 judge calls, all 44 returned a verdict; margins were 2 (6 calls),
3 (29 calls) and 4 (9 calls). Scoring mirrors the house: each call gives
the picked word 0.5 + margin/10 and the other the rest; a game's score is
the mean of its two calls.

Swiss standings (score / 3 games):

| Word | Score |
|---|---|
| **unsubscribed** | **2.55** |
| expired | 1.85 |
| recalled | 1.80 |
| placeholder | 1.55 |
| unread | 1.55 |
| refund | 1.50 |
| redacted | 1.50 |
| overdue | 1.50 |
| spam | 1.35 |
| beta | 1.30 |
| defective | 1.20 |
| draft | 1.15 |
| archived | 1.15 |
| demo | 1.05 |

Final (top 2): **unsubscribed 0.70 – 0.30 expired**. "unsubscribed" won
all 4 of its games, 8 of 8 judge calls — vs draft (margins 4, 4),
vs expired (3, 4), vs refund (3, 3), and the final vs expired (2, 2).
The judge's own words on it: *"frames the relationship as spam you
opted out of"* — instantly readable, funny, and a verdict, not an insult.

v1 shipped the pre-tournament favourite "recalled"; v2 replaces it with
the tournament winner "unsubscribed" and records the full results above.

## License

MIT — see `LICENSE`.

Referral code: 0txwmf1m
