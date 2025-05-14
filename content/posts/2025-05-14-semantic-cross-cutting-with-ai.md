---
date: '2025-05-13T19:48:32-07:00'
title: '🤖 Semantic Searching a Codebase'
tags: ['ai', 'productivity', 'code']
---

One useful facets of tools like [Cursor](https://cursor.com) is more readily finding the right file or function using more semantic searching. For example, I had suggested using a [partial index in Django](https://docs.djangoproject.com/en/5.2/ref/models/indexes/#django.db.models.Index.condition) and wanted to offer up examples in our codebase where we had used one. In the past, I've had to recall what files used one or come up with a somewhat complicated regex (remember to handle matches over newlines!) to locate examples. Now, I'm able to do a rather simple prompt with little added context:

> Search @models for examples of partial indexes

In my case, it didn't even need to be told that our codebase was Django!
