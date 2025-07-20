---
title: "Markdown Syntax Guide for Researchers - CMDS Obsidian Settings"
source: "https://slashpage.com/cmds-class/qpv5x4278nzg8mkyn3dw?full=1"
author:
  - "[[커맨드스페이스]]"
published: 2024-07-15
created: 2025-07-19
description: "Markdown Syntax Guide for Researchers Headings This is Heading 1 This is Heading 2 This is Heading 3 This is Heading 4 This is Heading 5 This is Heading 6 Basic Formatting Bold **볼드체 텍스트** or __볼드체 텍스트__ 볼드체 텍스트 Italic *이탤릭체 텍스트* or _이탤릭체 텍스트_ 이탤릭체 텍스트 Strikethrough ~~취소선 텍스트~~ 취소선 텍스트 Bold and Italic ***볼드체와 이탤릭체 함께*** or ___볼드체와 이탤릭체 함께___ 볼드체와 이탤릭체 함께 Lists Ordered List First item Second item"
tags:
  - "clippings"
---
## Markdown Syntax Guide for Researchers

Status

활용 단계

Created by

- 커맨드스페이스

Created at

## Markdown Syntax Guide for Researchers

## Headings

\# H1

\## H2

\### H3

\#### H4

\##### H5

\###### H6

## This is Heading 1

## This is Heading 2

### This is Heading 3

### This is Heading 4

### This is Heading 5

### This is Heading 6

## Basic Formatting

### Bold

\*\*볼드체 텍스트\*\* or \_\_볼드체 텍스트\_\_  
볼드체 텍스트

### Italic

\*이탤릭체 텍스트\* or \_이탤릭체 텍스트\_  
이탤릭체 텍스트

### Strikethrough

~~취소선 텍스트~~  
취소선 텍스트

### Bold and Italic

\*\*\*볼드체와 이탤릭체 함께\*\*\* or \_\_\_볼드체와 이탤릭체 함께\_\_\_  
볼드체와 이탤릭체 함께

## Lists

### Ordered List

1.First item

2.Second item

3.Third item

1.

First item

2.

Second item

3.

Third item

### Unordered List

\- First item

\- Second item

\- Third item

•

First item

•

Second item

•

Third item

### Task List

\- \[x\] Write the literature review

\- \[x\] Collect data

\- \[\] Analyze results

Write the literature review

Collect data

Analyze results

빵

우유

계란

논문리뷰

리비전 교정 표 만들고

## Code

### Inline Code

Use the \`print()\` function in Python.

Use the print() function in Python.  
기본적인 함수: y=f(x)  
Ctrl + y

### Code Block

\`\` \`python

def factorial(n):

if n == 0:

return 1

else:

return n \* factorial(n-1)

\` \`\`

def factorial (n):

if n \== 0:

return 1

else:

return n \* factorial (n \- 1)

## Links and References

### External Link

\[Markdown Guide\] (https://www.markdownguide.org)

![](https://www.youtube.com/watch?v=LxvbzoCfdw0)

### Internal Link (for tools that support it)

\[\[Research Methods\]\]

\[\[Research Methods\]\]  
\[\[🔖 Knowledge Connectivity\]\]

### Footnote

Here 's a sentence with a footnote.\[^1\]

  

\[^ 1\]: This is the footnote content.

Here's a sentence with a footnote.\[^1\]

\[^1\]: This is the footnote content.

내가 밥을 먹었는데 치킨이 먹고싶더라. \[^2\]

\[^2\]: 나의 감정을 표현한 글

## Quotes and Callouts

### Blockquote

\> This is a blockquote.

\> It can span multiple lines.

This is a blockquote.  
It can span multiple lines.

밥을 많이 먹으면 살이 찌더라.  
—구요한

### Nested Blockquotes

\> This is the first level of quoting.

\>

\> > This is nested blockquote.

\>

\> Back to the first level.

This is the first level of quoting.

This is nested blockquote.

Back to the first level.

## Images

!\[Alt text\] (image \- url.jpg "Optional title")

  
!\[\[Pasted image 20240627022953.png|400\]\]

## Tables

| Column 1 | Column 2 | Column 3 |

| \-- \-- \-- \-- \-- | \-- \-- \-- \-- \-- | \-- \-- \-- \-- \-- |

| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |

| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |

| A | B |
| --- | --- |
| 1 | 2 |

| Column 1 | Column 2 | Column 3 |
| --- | --- | --- |
| Row 1, Col 1 | Row 1, Col 2 | Row 1, Col 3 |
| Row 2, Col 1 | Row 2, Col 2 | Row 2, Col 3 |

## Horizontal Rule

\-- \-

## Mathematical Equations (LaTeX)

Many Markdown processors support LaTeX for mathematical equations.

### Inline Math

This is an inline equation: $E \= mc ^ 2 $

This is an inline equation: $E = mc^2$

### Display Math

This is a display equation:

  

$$

\\ frac { \\ partial f } { \\ partial x } \= 2 \\ sqrt { a } x

$$

This is a display equation:

$$  
\\frac{\\partial f}{\\partial x} = 2\\sqrt{a}x  
$$

근의공식:  
$$  
x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}  
$$

## Citations (for academic writing)

Some Markdown flavors (like Pandoc) support citations:

According to recent studies \[@ smith2023; @ johnson2022\], ...

## Abbreviations

The HTML specification is maintained by the W3C.

  

\* \[HTML\]: Hyper Text Markup Language

\* \[W3C\]: World Wide Web Consortium

The HTML specification is maintained by the W3C.

\*\[HTML\]: Hyper Text Markup Language  
\*\[W3C\]: World Wide Web Consortium

## Highlighting (supported in some flavors)

Here 's some ==highlighted text==.

Here's some ==highlighted text==.

Remember that support for some of these features (especially LaTeX equations, citations, and certain extensions) may vary depending on the Markdown processor or platform you're using. Always check your specific environment's capabilities and syntax requirements.

[Made with Slashpage](https://slashpage.com/)