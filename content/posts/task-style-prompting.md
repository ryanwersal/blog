---
title: "🎯 Task Style Prompting"
date: 2025-04-26T23:29:35Z
tags: ["ai", "prompting"]
---

There are many styles of prompting out there and one that recently caught my attention was what I've personally termed "task style prompting" or, more officially, [Decomposed Prompting](https://arxiv.org/abs/2210.02406). This is also conceputally similar to [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) though the former is more about maintaining an amount of state chat-to-chat while allowing usage of fresh context windows for each task. At least for coding based tasks it aligns well with the typical specification process: decompose the work into independent steps that can be executed in serial or, ideally, in parallel.

I've mostly found success by prompting to plan, strongly reconsider the plan, and emit a `TASK.md` file containing that plan. The biggest problem has been that each step is too ill specified, particularly if there are additional contextual files that must be included.
