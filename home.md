---
title: Wiki.js Test
description: 
published: true
date: 2020-08-05T04:54:10.371Z
tags: 
editor: markdown
---

# Intro

<a href="/vimcheatsheet.png"><img align="right" width=300 src="/vimcheatsheet.png"/></a>

List of things:
- This
- That
  - That over there
- The other
---
Task List:
- [x] Do a thing
- [ ] Do another thing
  - [x] Do this part of another thing
- [ ] Do all the things

# Tests

Various tests of features and functionality[^1]:

# Tabs {.tabset}

## Internal links list
This is a links list:
- [Test Page *Testing internal link to Test Page*](/test-page)
- [Secret Page *Testing link to hidden page*](/secret/diary)
{.links-list}

## Grid List
- This is the first item in a grid list
- A grid list just looks cool I guess
- I can't really do a sub-item
{.grid-list}

## Other tests

*[abbr]: Abbreviation

Testing abbr.[^longnote]

### Code block
```ruby
# Ruby syntax highlighting code block
if ruby_syntax == true
	puts "Good."
end
```

[^1]: Footnote test
[^longnote]: Abbreviations are defined like so:
	`*[abbr]: Abbreviation`
  