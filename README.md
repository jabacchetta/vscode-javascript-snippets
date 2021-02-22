# JavaScript Snippets (VSCode Extension)

[![Inline (VSCode extension) version badge](https://vsmarketplacebadge.apphb.com/version-short/jabacchetta.javascript-snippets.svg?color=blue&style=?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=jabacchetta.javascript-snippets)
[![Inline (VSCode extension) installs badge](https://vsmarketplacebadge.apphb.com/installs-short/jabacchetta.javascript-snippets.svg?color=blue)](https://marketplace.visualstudio.com/items?itemName=jabacchetta.javascript-snippets)
[![Inline (VSCode extension) rating badge](https://vsmarketplacebadge.apphb.com/rating-short/jabacchetta.javascript-snippets.svg?color=blue)](https://marketplace.visualstudio.com/items?itemName=jabacchetta.javascript-snippets)
[![MIT license badge](https://img.shields.io/badge/license-MIT-orange.svg?color=blue)](http://opensource.org/licenses/MIT)

## VSCode Masterclass (Coming Soon)

Follow [on Twitter](https://twitter.com/devcastcode) and [subscribe at DevCast](https://www.devcast.app/) to get priority access.

## Introduction

[JavaScript
Snippets](https://marketplace.visualstudio.com/items?itemName=jabacchetta.javascript-snippets) is a
collection of JavaScript code snippets that allow for ⚡ supercharged ⚡ auto-completions in VSCode.

## Features

* Modern JavaScript with features from ES10+.
* Strategically-ordered tabstops that take full advantage of IntelliSense.
* Placeholders only added where they a) represent required values and b) do not interfere with navigation or IntelliSense.
* Prefixes created with exact-match in mind, so that snippets do not need to be placed at the top of
  the suggestion list via modified VSCode settings (which would cause them to hide more relevant suggestions in some scenarios).
* Snippets are interchangeable and versatile, as opposed to monolithic, in order to prevent snippet
pollution.
* Avoids adding syntax that is best added manually (when it disrupts navigation or Intellisense).
* Includes snippets for commonly-needed utilities, which can be useful when experimenting in a scratch file or when
  working on small projects where you don't intend to import a JavaScript utility library (e.g.
  Lodash).
* Includes snippets for advanced console logs that are colorized, grouped, and edge-case-resistant.

## Style

These snippets follow the [Airbnb style guide](https://github.com/airbnb/javascript), valuing code
  safety, clarity, and low maintenance above all else. Brevity is preferred, but only when it does
  not negate the aforementioned objectives.

Not a fan of Airbnb's style guide? No problem, you can still use these snippets along with
  [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) to have
  your code automatically formatted with your preferences.

## Removing Snippets

To disable VSCode's built-in JavaScript snippets (which are lacking and — when combined with
this snippet pack — redundant), use the [Control
Snippets](https://marketplace.visualstudio.com/items?itemName=svipas.control-snippets) extension.

## Recommended Settings

```jsonc
{

  // Allows for tab completion of snippets even when quick suggestion list is not displayed.
  "editor.tabCompletion": "onlySnippets",

  "[javascript]": {
    // Keyword completions aren't that useful by themselves, and they appear above more useful
    // snippets when `editor.snippetSuggestions` is not set to `top`.
    "editor.suggest.filteredTypes": {
      "keyword": false,
    },
  },
}
```

## Other Relevant Settings

```jsonc
{
  // // Obviously makes snippets easier to find and select, but pushes more-relevant suggestions down
  // // the list in some scenarios. Leaving this set to the default of `inline` will still almost
  // // always result in snippets being at the top when you expect them to (assuming there aren't
  // // other completions with the same exact-match as the snippet prefix).
  // "editor.snippetSuggestions": "top",

  // // By default, when in an active snippet, quick suggestions do not automatically appear. Instead,
  // // you're required to manually trigger IntelliSense. Enabling the following setting will allow
  // // suggestions to automatically appear, but it will also make navigating through tabstops
  // // inconvenient (you'll need to accept a suggestion or close the list before moving to the next
  // // tabstop). An alternate solution is to change the keybinding for `jumpToNextSnippetPlaceholder`,
  // // so that you're not using tab to simultaneously navigate through both suggestions and tabstops
  // "editor.suggest.snippetsPreventQuickSuggestions": false,
}
```

## Included Snippets

### Array

| Prefix | Title | Description |
| --- | --- | --- |
| `am` | arrayMerge | Shallow-copy a single array (clone) or multiple arrays (merge) to a new array literal via the spread operator. |
| `range` | range | An array containing a sequence of numbers from 0 up to, but not including, length. |
| `uniq` | uniq | Creates a duplicate-free version of an array. |
| `foreach` | forEach | Array.prototype.forEach() method. |
| `map` | map | Array.prototype.map() method. |
| `reduce` | reduce | Array.prototype.reduce() method. |
| `reduceright` | reduceRight | Array.prototype.reduceRight() method. |
| `filter` | filter | Array.prototype.filter() method. |
| `find` | find | Array.prototype.find() method. |
| `findindex` | findIndex | Array.prototype.findIndex() method. |
| `some` | some | Array.prototype.some() method. |
| `every` | every | Array.prototype.every() method. |
| `flatmap` | flatMap | Array.prototype.flatMap() method. |

### Assignment

| Prefix | Title | Description |
| --- | --- | --- |
| `ca` | constAssignment | Const assignment.
| `la` | letAssignment | Let assignment. |
| `cad` | constAssignmentDestructuring | Const object destructuring assignment. |
| `lad` | letAssignmentDestructuring | Let object destructuring assignment. |

### Class

| Prefix | Title | Description |
| --- | --- | --- |
| `cs` | class | Class exported as default and named after the file (if file is not named index, in which case the class is named after the parent folder). |
| `cse` | classExtends | Subclass exported as default and named after the file (if file is not named index, in which case the class is named after the parent folder). |
| `ctr` | constructor | Class constructor. |
| `met` | method | Class method. |

### Conditional

| Prefix | Title | Description |
| --- | --- | --- |
| `if` | if | If statement. |
| `el` | else | Else statement. |
| `ei` | elseIf | Else-if statement. |
| `ter` | ternary | Ternary operator. |
| `switch` | switch | Switch statement. |
| `case` | case | Case clause. |

### Console

| Prefix | Title | Description |
| --- | --- | --- |
| `cl` | consoleLog | Console log. |
| `ce` | consoleError | Console error. |
| `cw` | consoleWarn | Console warn. |
| `clc` | consoleLogClipboard | Console log the value you have copied to your clipboard, inside of an object (for an automatic label). |
| `clm` | consoleLogMessage | Console log a message. |
| `clo` | consoleLogObject | Console log an object, in which variables can be inserted (for automatic labels). |
| `clr` | consoleLogReturn | Console log. Appended by the logical OR operator (for convenient logging in front of an arrow function's implicit return value). |
| `clmr` | consoleLogMessageReturn | Console log message. Appended by the logical OR operator (for convenient logging in front of an arrow function's implicit return value). |
| `clor` | consoleLogObjectReturn | Console log an object, in which variables can be inserted (for automatic labels). Appended by the logical OR operator (for convenient logging in front of an arrow function's implicit return value). |
| `clg` | consoleLogGroup | Console log, wrapped in a formatted and styled console group. |
| `cla` | consoleLogAnalysis | Console log an object, in which variables can be inserted. Includes value, type, count, and trace for all values. Includes log-time value and table for objects. Wrapped in a formatted and styled console group. |

### Exception

| Prefix | Title | Description |
| --- | --- | --- |
| `tc` | tryCatch | Try-catch statement. |
| `tcf` | tryCatchFinally | Try-catch-finally statement. |
| `tf` | tryFinally | Try-finally statement. |
| `te` | throwError | Throw error object exception. |

### Function

| Prefix | Title | Description |
| --- | --- | --- |
| `function` | function | Named function declaration. |
| `af` | arrowFunction | Anonymous arrow function expression. |

### JSON

| Prefix | Title | Description |
| --- | --- | --- |
| `jp` | jsonParse | JSON.parse() method. |
| `js` | jsonStringify | JSON.stringify() method. |

### Loop

| Prefix | Title | Description |
| --- | --- | --- |
| `dowhile` | doWhile | Do-while loop. |
| `while` | while | While loop. |
| `for` | for | For loop. |
| `forin` | forIn | For-in loop. |
| `forof` | forOf | For-of loop. |

### Miscellaneous

| Prefix | Title | Description |
| --- | --- | --- |
| `use` | useStrict | Use strict statement. |

### Module

| Prefix | Title | Description |
| --- | --- | --- |
| `imp` | import | Import module. |
| `expd` | exportDefault | Default export. |
| `exp` | export | Named export. |

### Object

| Prefix | Title | Description |
| --- | --- | --- |
| `om` | objectMerge | Shallow-copy a single object (clone) or multiple objects (merge) to a new object literal via the spread operator. Similar to the Object.assign() method, but has the added benefit of not allowing for shallow mutations. |
| `oe` | objectEntries | Object.entries() method. |
| `ofe` | objectFromEntries | Object.fromEntries() method. |
| `ok` | objectKeys | Object.keys() method. |
| `ov` | objectValues | Object.values() method. |

### Return

| Prefix | Title | Description |
| --- | --- | --- |
| `ret` | return | Return statement. |
| `retm` | returnMultiline | Return statement for multiline expression that includes complex values (e.g. JSX). |

### Scheduler

| Prefix | Title | Description |
| --- | --- | --- |
| `st` | setTimeout | setTimeout() method. |
| `si` | setInterval | setInterval() method. |

### Type

| Prefix | Title | Description |
| --- | --- | --- |
| `to` | typeof | typeof operator. |
| `io` | instanceof | instanceof operator. |
| `aia` | arrayIsArray | Array.isArray() method. |
| `isplainobject` | isPlainObject | Check if value is a plain object. |
| `isnil` | isNil | Check if value is null or undefined. |
