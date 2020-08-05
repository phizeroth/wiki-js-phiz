---
title: Wiki.js Test
description: 
published: true
date: 2020-08-05T04:42:20.330Z
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

# Tests {.tabset}

Various tests of features and functionality[^1]:

## Internal link tests

Testing internal link to [Test Page](/test-page).

Testing link to [Secret Page](/secret/diary).

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
  