# Disallow multiple access of same DOM element (`@ecocode/no-multiple-access-dom-element`)

⚠️ This rule _warns_ in the ✅ `recommended` config.

<!-- end auto-generated rule header -->

## Rule details

This rule aims to reduce DOM access assigning its object to variable when access multiple time. It saves CPU cycles.

## Examples

Examples of **incorrect** code for this rule:

```js
var el1 = document.getElementById("block1").test1;
var el2 = document.getElementById("block1").test2;
```

Examples of **correct** code for this rule:

```js
var blockElement = document.getElementById("block1");
var el1 = blockElement.test1;
var el2 = blockElement.test2;
```
