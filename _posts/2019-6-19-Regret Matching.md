---
layout: post
categories: AI
---

#### 概念
**regret matching**: an agents actions are
selected at random with a distribution that is _**proportional to positive regrets**_.

minimal regret strategy is the average strategy across all iterations.

#### 示例
[RPSTrainer](https://heartup.github.io/static/raw/RPSTrainer.zip)

#### Kuhn Poker's Information Set
P0 has 6 IS:
- no one has actioned, P0 was dealed card0, card1 or card2 (3 IS)
- P0 pass, P1 bet, P0 was dealed card0, card1 or card2 (3 IS)

P1 has 6 IS:
- P0 pass, P1 was dealed card0, card1 or card2 (3 IS)
- P1 bet, P1 was dealed card0, card1 or card2 (3 IS)