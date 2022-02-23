---
bookCollapseSection: false
title: "Installation"
weight: 1
---
# Installation

The following guide is for installing Hugo on macOS.

## Step 1: Update homebrew

```console
$ git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow -v
```
<button onclick="copyToClipboard('excode_homebrew_update_core')">Copy</button>
<p id="copied_alert_excode_homebrew_update_core" style="display: none; color: green">Copied!</p>

```console
$ git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask fetch --unshallow -v
```
<button onclick="copyToClipboard('excode_homebrew_update_cask')">Copy</button>
<p id="copied_alert_excode_homebrew_update_cask" style="display: none; color: green">Copied!</p>

## Step 2: Install Hugo with brew

```console
$ brew install hugo
```
<button onclick="copyToClipboard('excode_install_hugo_global')">Copy</button>
<p id="copied_alert_excode_install_hugo_global" style="display: none; color: green">Copied!</p>

## Step 3: Create a base Hugo project

```console
$ hugo new site my-hugo-site
```
<button onclick="copyToClipboard('excode_new_hugo_project')">Copy</button>
<p id="copied_alert_excode_new_hugo_project" style="display: none; color: green">Copied!</p>


## Step 4: Add the hugo-book theme

First, navigate into your site directory.

```console
$ cd my-hugo-site
```

Then, initialize a git repo and add the hugo-book theme.

```console
$ git init && git submodule add https://github.com/alex-shpak/hugo-book themes/hugo-book
```
<button onclick="copyToClipboard('excode_install_hugo_book_theme')">Copy</button>
<p id="copied_alert_excode_install_hugo_book_theme" style="display: none; color: green">Copied!</p>

## Step 5: Create your pages

```console
$ hugo new docs/welcome.md
```
<button onclick="copyToClipboard('excode_create_hugo_book_page')">Copy</button>
<p id="copied_alert_excode_create_hugo_book_page" style="display: none; color: green">Copied!</p>

## Troubleshooting

#### Error with brew

Run `brew update` and follow the instructions.

#### Error with hugo

Refer to the [hugo source documentation](https://gohugo.io/getting-started/).

#### Error with hugo-book theme

Refer to the [hugo-book source documentation](https://themes.gohugo.io/themes/hugo-book/).


<script>
function copyToClipboard(id) {
  const code_snippets = {
    excode_homebrew_update_core: 'git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow -v',
    excode_homebrew_update_cask: 'git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask fetch --unshallow -v',
    excode_install_hugo_global: 'brew install hugo',
    excode_new_hugo_project: 'hugo new site my-hugo-site',
    excode_install_hugo_book_theme: 'git init && git submodule add https://github.com/alex-shpak/hugo-book themes/hugo-book',
    excode_create_hugo_book_page: 'hugo new docs/welcome.md',
  };
  const ids = Object.keys(code_snippets);
  navigator.clipboard.writeText(code_snippets[id]);
  document.getElementById(`copied_alert_${id}`).style.display = 'block';
  ids
    .filter(i => i !== id)
    .forEach(i => document.getElementById(`copied_alert_${i}`).style.display = 'none');
}
</script>