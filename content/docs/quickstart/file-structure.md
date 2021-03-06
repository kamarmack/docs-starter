---
title: "File Structure"
weight: 2
---
# File Structure

## Menu

The hugo-book theme provides a tree-like menu structure that you can use to organize your documentation.

```
├── docs
│   ├── section
│   │   ├── _index.md
│   │   ├── nested-01.md
│   │   ├── nested-02.md
│   │   ├── nested-03.md
│   ├── top-level-01.md
│   ├── top-level-02.md
│   ├── top-level-03.md
```

By default, pages in the base `docs/` directory will appear at top level of the table of contents with no children.

In order to group pages into a section, create a `docs/section/_index.md` file and then populate that directory with your related pages.

The theme also supports the usage of posts, but this is not explored.

## Page Options

These are the most important config options that control the page UI.

| Property | Value | Default Value | Description |
| ------ | ------ | ------ | ------ |
| bookCollapseSection | `boolean` | `false` | Whether the menu should collapse a section of pages. **Note**: If you set the `bookCollapseSection` property of a section's `_index.md` file to `true`, then you must manually set the `bookCollapseSection` property to `false` in each of the section's pages. Otherwise, the menu will collapse the section even after one of the pages is selected. |
| bookSearchExclude | `boolean` | `false` | Whether to exclude the page from search. |
| bookToc | `boolean` | `true` | Whether to show a secondary table of contents for this page's markdown sections on the right side of the page. |
| title | `string` | NA | Title of the page. Used in the primary table of contents and the browser bar. |
| weight | `number` | NA | Determines this page's order in the primary table of contents. Weight is scoped to a section. |
