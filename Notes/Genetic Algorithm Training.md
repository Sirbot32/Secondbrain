---
tags: [ai]
topic: AI
created: 2026-06-22
status: confirmed
---

# Genetic Algorithm Training

When there's no labeled "correct" output to learn from — like training a bot to trade in a predictive market — one approach is to generate a large number of random strategies, run them against a performance threshold, and let the strategies that succeed produce "children" similar to themselves but with some weights mutated. Repeating this over many generations gradually improves the strategies.

This is a real training method (a genetic/evolutionary algorithm), but it's not how most large neural networks — including LLMs — are actually trained. That's typically done with backpropagation/gradient descent instead (see Learning Queue).

Related: [[Neural Network Weight]]
