---
title: "🗣️ Prompt Engineering: Speaking AI's Language"
date: 2025-04-23T14:00:00-07:00
draft: false
tags: ["ai", "prompts", "engineering"]
categories: ["ai"]
---

I went into yesterday and today expecting to dive into prompt engineering - crafting meticulous and targeted AI language to effectively "program" the AI and its responses. However, that is not what happened - at all.

In fact, the prompting exercise was this blog and was created exclusively in [Cursor](https://cursor.com) using incredibly _simple_ prompts. Perfectly natural language even! It was hardly programming of any variety.

A few example prompts from the exercise:

> I want to create a blog using Hugo.

That got me the blog and even installed the `hugo` CLI along with the basic scaffolding from initializing a new blog site. However, I had noticed that the About and Archive pages were both showing up in the Archive page listing instead of only blogs. Shockingly, the following prompt resolved the issue:

> The archive page is showing up in the archive page.

No material context. No suggestion on what the problem is or a proposed fix. But it figured out the _intent_ and solved the problem by filtering to only blog posts.

Finally, I noticed the default favicon and wanted to use my usual, which is readily fetched from Gravatar. The following prompt knocked out a quick `bash` script to `curl` the image and placed it into the right static directory and it was done in about a minute.

> Fetch the gravatar for <my email> and use it as the site's favicon.

---

That takes me into today: what about [Cursor Rules](https://docs.cursor.com/context/rules) and similar more system-style prompts? What are the important traits of successful system prompts?

Fortunately there's plenty of examples out there. `sharkgwy` has a [repo containing an old version of the v0 prompt](https://github.com/sharkqwy/v0prompt/blob/main/prompt.txt). There's also the [System Prompts & Models of AI Tools](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) repo from `x1xhlol` with an extensive array of system prompts, including a more current v0 prompt.

A few quick takeaways:

- Most of the prompting feels _under_ prompted. There's a lot of "whitespace" for the AI to operate in. 
- The minimal prompting is probably for [reducing token counts](https://github.com/openai/tiktoken?tab=readme-ov-file#-tiktoken) but there are certainly counter examples such as [this verbose example of Mermaid in v0's prompt](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools/blob/main/v0%20Prompts%20and%20Tools/v0.txt#L167-L180).
- The prompt is heavily structured around constraints rather than capabilities. It's full of "MUST" and "NEVER" statements that define boundaries rather than explaining what's possible.

[OpenAI](https://openai.com) has a [fantastic section on prompt engineering](https://platform.openai.com/docs/guides/text?api-mode=responses#prompt-engineering). I found the [Few Shot Learning](https://platform.openai.com/docs/guides/text?api-mode=responses#few-shot-learning) section of particular interest as it explains the example-laden style employed in the system prompts.
