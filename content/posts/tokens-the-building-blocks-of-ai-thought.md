---
title: "🧩 Tokens: The Building Blocks of AI Thought"
date: 2025-04-22T21:00:00Z
draft: false
tags: ["ai", "nlp", "tokenization"]
categories: ["ai"]
---

Understanding how AI models break down text into tokens is crucial - it's literally how they think, process costs are measured by it, and getting it wrong can lead to some hilariously bad outputs. Here are some interesting resources about tokenization that I dove into today:

[OpenAI Tokenizer](https://platform.openai.com/tokenizer). This highlighted some interesting takeaways:
- On average, a single token is about four characters.
- Many symbols, at least visually, consume a token. Is that why [system prompts](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) seem to shy away from symbols? (Except when [they don't](https://github.com/sharkqwy/v0prompt/blob/main/prompt.txt).)

[tiktoken - Byte Pair Encoding (BPE)](https://github.com/openai/tiktoken?tab=readme-ov-file#what-is-bpe-anyway) came up in a conversation about "compressing" tokens / prompts.
