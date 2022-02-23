---
title: "Welcome"
weight: 1
---
# Welcome

## Introduction

Welcome to **Docs Starter**. I'm a nice base project for markdown documentation forked from <a href="https://themes.gohugo.io/themes/hugo-book/" target="_blank">Hugo Book</a>.

Refer to [Quickstart Installation](/docs/quickstart/installation) to create documentation for your software.

## `Welcome.md` File

This example file has some introductory markdown content. Use it to write a *overview* about your software. Then provide details and implementation steps in your subsequent files.

Notice the weight in the Hugo "front" section of this file is `1`, so it appears at the top of the table of contents, even though alphabetically it should be near the bottom.

## Use Cases

Docs Starter is excellent for software that changes infrequently such as a narrow use-case internal tool. For such scenarios, Docs Starter excels at the following tasks:

- Serving as a scratchpad during development
- Serving as a quick installation guide or API reference post-development

## Limitations

Docs Starter is **not** optimized to be programmatically generated and updated alongside your changes to an underlying code base / repo. Therefore, it is **not** suitable for software that changes frequently or customer-facing products.

Secondly, the copy-paste functionality for code snippets is currently implemented by writing a `copyToClipboard` function in each file that contains code. This obviously does not scale.

## Additional Example

For an additional example file, refer to the dummy [Advanced Usage](/docs/advanced-usage) page.
