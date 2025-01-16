---
count: 10
distance: 
c: 0
completed: false
rating: trash
numeric_rating: 2
---

```meta-bind-button
style: primary
label: Meta Bind Help
action:
  type: command
  command: obsidian-meta-bind-plugin:mb-open-faq
```

Meta Bind has an in plugin help page. `BUTTON[help-button]` Isn't that cool?

Theme Switcher: `BUTTON[light-mode, dark-mode]`
***POTS***: `VIEW[{count}]`  |   `BUTTON[count-decrement, count-increment]` 
***POTS***: `VIEW[{count} km]`  |   `BUTTON[count-decrement, count-increment]`
***POTS***: `INPUT[number:count]` `BUTTON[count-decrement, count-increment]`
***POTS***: `VIEW[$\left\[\kern5px{count}\kern5px\right\]$][text(renderMarkdown)]` `BUTTON[count-decrement, count-increment]`

generic toogle: `INPUT[toggle]`
completed toogle: `INPUT[toggle:completed]`

```meta-bind
INPUT[inlineSelect(
    option(trash),
    option(bad),
    option(ok),
    option(good),
    option(great)
):rating]
```

```meta-bind
INPUT[inlineSelect(
    option(1, trash),
    option(2, bad),
    option(3, ok),
    option(4, good),
    option(5, great)
):numeric_rating]
```

###########
#### TE
#### BUTTON
# Button


---

let str = '*test*';
return str;

```meta-bind-button
style: primary
label: Greet the World
action:
  type: inlineJS
  code: "console.log('Hello World!');"
```

---
View:
***Usage***: VIEW\[content\]\[viewFieldType\]
`VIEW[{a} * {b}]`
`VIEW[{a} * {b}][math]`
`VIEW[**{someText}**][text(renderMarkdown)]`
`VIEW[{a} * {b}][math:c]`

```meta-bind-button
style: primary
label: RexExp Replace In Note
action:
  type: "regexpReplaceInNote"
  regexp: "```meta-bind-button\nstyle: primary\nlabel: RexExp Replace In Note\naction:\n  type: \"regexpReplaceInNote\"\n  regexp: \"(TODO: .*)\\n\"\n  replacement: \"$1 - Done\"\n```"
  replacement: "BOH"
```

[[Clickable Empty Check]]

```meta-bind-button\nstyle: primary\nlabel: RexExp Replace In Note\naction:\n  type: \"regexpReplaceInNote\"\n  regexp: \"(TODO: .*)\\n\"\n  replacement: \"$1 - Done\"\n```

```meta-bind-button\nstyle: primary\nlabel: RexExp Replace In Note\naction:\n  type: \"regexpReplaceInNote\"\n  regexp: \"(TODO: .*)\\n\"\n  replacement: \"$1 - Done\"\n```


---
###### Reference Buttons
```meta-bind-button
style: destructive
label: Light Mode
id: light-mode
hidden: true
actions:
  - type: command
    command: theme:use-light
```

```meta-bind-button
style: primary
label: Dark Mode
id: dark-mode
hidden: true
actions:
  - type: command
    command: theme:use-dark
```

```meta-bind-button
style: primary
label: Meta Bind Help
id: help-button
action:
  type: command
  command: obsidian-meta-bind-plugin:open-faq
```


```meta-bind-button
label: "+1"
hidden: true
id: "count-increment"
style: default
actions:
  - type: updateMetadata
    bindTarget: count
    evaluate: true
    value: x + 1
```

```meta-bind-button
label: "-1"
hidden: true
id: "count-decrement"
style: default
actions:
  - type: updateMetadata
    bindTarget: count
    evaluate: true
    value: x - 1
```

```meta-bind-button
label: "Reset"
hidden: true
id: "count-reset"
style: default
actions:
  - type: updateMetadata
    bindTarget: count
    evaluate: false
    value: 0
```

