---
title: Wiki.js Test
description: 
published: true
date: 2020-08-05T05:34:14.469Z
tags: 
editor: markdown
---

# Intro

<a href="/vimcheatsheet.png"><img align="right" width=300 src="/vimcheatsheet.png"/></a>

**List of things**
- This
- That
	- That over there
- The other
---
**Task List** :sweat:
- [x] Do a thing
- [ ] Do another thing
  - [x] Do this part of another thing
- [ ] Do all the things

# Tests

Various tests of features and functionality:

## Tabs {.tabset}

### Internal links list
This is a links list:
- [Test Page *Testing internal link to Test Page*](/test-page)
- [Secret Page *Testing link to hidden page*](/secret/diary)
- [SmartThings Button *Page with some actual content*](/iot/home-automation/smartthings-button)
{.links-list}

### Grid List

This is called a grid list:
- This is the first item in a grid list
- A grid list just looks cool I guess
- Nice alternating shades
- Interesting stuff
{.grid-list}
  - I can even do indented sub-items if I'm feeling particularly frisky
  - Like so, you see, yes indeed
  - |well|looky|
    |-|-|
    |I can|just plop|
    |a table|in here|
    |if i feel|like it|
- And that just about wraps that up

### Code block
```ruby
# Ruby syntax highlighting code block
if ruby_syntax == true
	puts "Good."
end
```

### Other tests

#### Keyboard keys

Press <kbd>Alt</kbd> + <kbd>F4</kbd> for a good time.
<br />

#### Abbreviations[^longnote]
*[abbr]: Abbreviation 

This is an abbr.

[^longnote]: Abbreviations are defined like so:
	`*[abbr]: Abbreviation`

  