---
title: "🎯 Task Style Prompting"
date: 2025-05-12T23:29:35Z
tags: ["ai", "prompting"]
---

I've been futzing with what I call "task style prompting" recently (it appears likely to be better known as [Decomposed Prompting](https://arxiv.org/abs/2210.02406)). It's conceptually similar to [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) though the former is more about maintaining an amount of state chat-to-chat while allowing usage of fresh context windows for each task. At least for coding based tasks it aligns well with the typical specification process: decompose the work into independent steps that can be executed in serial or, ideally, in parallel.

I've mostly found success by prompting for a plan, to strongly reconsider the plan, and emit a `TASK.md` file containing that plan. The biggest problem has been that each step can be too ill specified, particularly if there are additional contextual files that must be included to accomplish the task (all too often the fresh context was missing critical details on _how_ to produce the code).
