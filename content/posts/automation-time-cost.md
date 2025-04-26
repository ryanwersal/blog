---
title: "🤖 Diminishing Time Costs of Automation"
date: 2025-04-25T10:00:00-07:00
draft: false
tags: ["automation", "ai", "productivity"]
categories: ["ai"]
---

Today I wrote a [Cursor Rule](https://docs.cursor.com/context/rules#project-rules) that mapped out how to upgrade an archetype of our Node projects. They're relatively small, strongly follow conventions, and are essentially purpose built to be automatable by AI. A prime target. And it worked!

The rule handles modernizing those projects - each one individually. This involves updating dependencies for our own packages but also working through a couple TypeScript breaking changes and swapping out one set of tools (`eslint` and `prettier`) for another (`biome`). This sort of thing has always been automatable, but unfortunately projects like these tend to drift in tiny and very nuanced ways, which drives up the time to successfully automate.

The fact that a Cursor Rule, ~70 lines of prompt engineering (yes, engineering [this time](./prompt-engineering-speaking-ai-language.md) as, oh my, trying to convince the AI to not hallucinate package versions or assume the latest is whatever was latest at its [knowledge cutoff](https://computercity.com/artificial-intelligence/knowledge-cutoff-dates-llms) was quite the _chore_; protip: tell it to use `npm view` to identify latest versions!), could not only automate the broad strokes but leave enough _wiggle room_ for the AI to respond to compile or linter errors or identify unused dependencies was magnificent! AI editing opens the door to a broader swath of _semantic_ refactoring.

This situation reminded me of [kxcd 1205](https://xkcd.com/1205/) about automation and the amount of time that must be saved before the endeavor was nothing but converting a chore into fun.

[![xkcd 1205: Is It Worth the Time?](/images/is_it_worth_the_time.png)](https://xkcd.com/1205/)

I reflected on how AI has dramatically shifted that level of effort. So many more tasks are now automatable in a way that produces _value_ beyond the fun of avoiding the chore.

You no longer have to meticulously craft code to handle every novel case you run into. You no longer expect to make a tweak or two to the script for each project touched by this automation! And if adjustments are required? You can interact with the _current state_ of the AI in chat and iterate on how to express fixing that problem. Cursor even added a feature recently to [convert that context into rules](https://www.cursor.com/changelog/0-49) once you've got a bead on a solution.

I'll certainly be on the lookout for further automation opportunities!
