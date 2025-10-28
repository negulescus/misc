# Markdown Feature Showcase

## Headings

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

## Emphasis

```
*Italic* or _Italic_    
```
*Italic* or _Italic_  
```
**Bold** or __Bold__  
```
**Bold** or __Bold__  
```
***Bold and Italic***  
```
***Bold and Italic***  
```
~~Strikethrough~~  
```
~~Strikethrough~~  

Note: underline is not available in markdown

## New Lines and Paragraphs

To add a new line on the same paragraph after this one (with a line break) use two spaces at the nd of this line after the dot.  
This is a new line. The line above it has two spaces at the end.

This is a new paragraph.  
It starts after a blank line.

Another paragraph follows here.

## Lists

### Unordered List

```
- Item 1  
- Item 2  
  - Subitem 2.1  
  - Subitem 2.2
```
- Item 1  
- Item 2  
  - Subitem 2.1  
  - Subitem 2.2

Note: to indent the list use two spaces in front of the items.

### Ordered List

```
1. First  
2. Second  
   1. Sub-second  
   2. Sub-third
```
1. First  
2. Second  
   1. Sub-second  
   2. Sub-third

Note: to indent the list use two spaces in front of the items.

## Links

```
[External Website Example](https://github.com/negulescus/misc/blob/main/Markdown%20Feature%20Showcase.md)[Relative link to a heading inside this BookStack document -> Headings](#bkmrk-headings)  
[Relative link to a heading inside this document -> Headings](#headings)  
Less preffered mode: <https://example.com>
```
[External Website Example](https://github.com/negulescus/misc/blob/main/Markdown%20Feature%20Showcase.md)  
[Relative link to a heading inside this BookStack document -> Headings](#bkmrk-headings)  
[Relative link to a heading inside this document -> Headings](#headings)  
Less preffered mode: <https://example.com>

## Images

```
![Placeholder Image](hhttps://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)
```
![Placeholder Image](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

## Code

### Inline Code

```
Use `code()` to call a function.
```
Use `code()` to call a function.

### Code Block

````
```python
def hello_world():
    print("Hello, world!")
```
````  
Result:  
```python
def hello_world():
    print("Hello, world!")
```

## Blockquotes

```
> This is a blockquote.  
>> Nested blockquote.
>>> 3rd level nesting.
```

> This is a blockquote.  
>> Nested blockquote.
>>> 3rd level nesting.

## Horizontal Rule

```
---
```
---

## Tables

```
| Left Align | Center Align | Right Align | Default Align |
|:-----------|:------------:|------------:|---------------|
| Apple      | Banana       | $1.00       | abc           |
| Orange     | Kiwi         | $2.50       | def           |
| Grapes     | Mango        | $3.75       | ghi           |
```
Note: the extra spaces to align the charactes in the example above are optional.

| Left Align | Center Align | Right Align | Default Align |
|:-----------|:------------:|------------:|---------------|
| Apple      | Banana       | $1.00       | abc           |
| Orange     | Kiwi         | $2.50       | def           |
| Grapes     | Mango        | $3.75       | ghi           |

## Task Lists

```
- [x] Write Markdown  
- [ ] Review content  
- [ ] Submit document
```
- [x] Write Markdown  
- [ ] Review content  
- [ ] Submit document

## HTML in Markdown

```
<div style="color: red;">This is red text.</div>
This&nbsp;text&nbsp;contains&nbsp;non-breaking&nbsp;spaces&nbsp;between&nbsp;words.
```

<div style="color: red;">This is red text.</div>
This&nbsp;text&nbsp;contains&nbsp;non-breaking&nbsp;spaces&nbsp;between&nbsp;words.
Note: please avoid using html in markdown.

## Footnotes

```
Here is a sentence with a footnote.[^1]

[^1]: This is the footnote.
```

Here is a sentence with a footnote.[^1]

[^1]: This is the footnote.

## Emoji (GitHub-flavored)

```
:smile: :rocket: :+1:  
The above might not wotk in all markdown editors.  
You may use UTF8 characters.  
📘 (Guideline), 📋 (Log), 📄 (Template), 📜 (Policy), 🗂️ (Record), 📝 (Procedure), 📁 (Process), 📂 (Role)
```
:smile: :rocket: :+1:  
The above might not wotk in all markdown editors.  
You may use UTF8 characters.  
📘 (Guideline), 📋 (Log), 📄 (Template), 📜 (Policy), 🗂️ (Record), 📝 (Procedure), 📁 (Process), 📂 (Role)

## Escaping Characters

```
\*This text is not italic\*  
```

\*This text is not italic\*  
Note: the backslash charater is used for escaping.
