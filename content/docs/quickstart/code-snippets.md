---
bookCollapseSection: false
bookToc: false
title: "Code Snippets"
weight: 3
---
## Code snippets

Here's a quick illustratation of adding copy-and-pastable code snippets to your documentation.

JavaScript example <button onclick="copyToClipboard('excode_js_array')">Copy</button>

```javascript
const array = [1, 2, 3];
console.log(array);
```
<p id="copied_alert_excode_js_array" style="display: none; color: green">Copied!</p>

> Here's an example warning that could be used for instance for versioning notes

TypeScript example <button onclick="copyToClipboard('excode_ts_types')">Copy</button>

```typescript
type User = {
  id: string;
  name: string;
  balance: number;
};
type Customer = User & {
  status: 'paid' | 'trialing';
};
```
<p id="copied_alert_excode_ts_types" style="display: none; color: green">Copied!</p>

Bash command example
```console
$ whoami
```
<button onclick="copyToClipboard('excode_console_user_check')">Copy</button>
<p id="copied_alert_excode_console_user_check" style="display: none; color: green">Copied!</p>

JSON example <button onclick="copyToClipboard('excode_json_username_pass')">Copy</button>

```json
{
  "pass": "kinda-complicated-but-nice-when-it-works",
  "username": "hugo"
}
```
<p id="copied_alert_excode_json_username_pass" style="display: none; color: green">Copied!</p>

<script>
function copyToClipboard(id) {
  const code_snippets = {
    excode_js_array: `const array = [1, 2, 3];
console.log(array);`,
    excode_ts_types: `type User = {
  id: string;
  name: string;
  balance: number;
};
type Customer = User & {
  status: 'paid' | 'trialing';
};`,
    excode_console_user_check: 'whoami',
    excode_json_username_pass: `{
  "pass": "kinda-complicated-but-nice-when-it-works",
  "username": "hugo"
}`,
  };
  const ids = Object.keys(code_snippets);
  navigator.clipboard.writeText(code_snippets[id]);
  document.getElementById(`copied_alert_${id}`).style.display = 'block';
  ids
    .filter(i => i !== id)
    .forEach(i => document.getElementById(`copied_alert_${i}`).style.display = 'none');
}
</script>