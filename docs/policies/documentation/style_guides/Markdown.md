# Style Guides: Markdown

## Headings

### Only One Level One Heading

There MUST be a single level one header at the beginning of each document. It MUST follow immediately after any metadata, such as Frontmatter. This heading serves as the title for the document. If `title` metadata is peresnt this heading and the metadata MUST be identical.

### Headings Levels Increment One Level at a Time

Headings MUST increase nesting by only one level at a time. They MAY decrease by any number of levels.

**Valid example**:

```markdown
# Title

## Level 2

### Level 3

### Another Level 3

#### Level 4

## Another Level 2
```

**Invalid Example**:

```markdown
# Title

## Level 2

#### Level 4 <- Level 3 was skipped
```

### Use ATX Headings Without Closing Markers

Headings MUST only use the ATX style without trailing whitespace or closing markers. The ATX style is from one to six "&num;" characters followed by a single space and the text of the heading. There MUST be no trailing spaces or punctuation.

```markdown
# Level 1 Heading

## Level 2 Heading

### Level 3 Heading

#### Level 4 Heading

##### Level 5 Heading

###### Level 6 Heading
```

### Headings are Surrounded by Blank Lines

Headings, with the exception of the initial level one heading, MUST be preceeded by and followed by exactly one blank line.

### Headings Start at the Beginning of the Line

Headings MUST NOT be preceeded by any indentation or white space.

_Note_: Scenarios like block quotes "indent" the start of the line, so the following is correct:

```markdown
> # Heading in Block Quote
```

### Sibling Headings Are Different

Headings at the same level under another heading MUST be different.

## Lists

List markers MUST start at the beginning of the line _or_ at a multiple of four spaces of indentation. There MUST be one space after the list marker. List marker types MUST NOT be mixed at the same level of list.

Lists MUST be preceeded and followed by one blank line.

### Unordered Lists

All three Markdown list markers (dash, asterisk, and plus) MAY be used. Nested lists MUST use a different marker than their parent.

**Examples**:

```markdown
-   Item 1
```

```markdown
-   Item 2
```

```markdown
-   Item 3
```

**Nested list example**:

```markdown
-   Item 1
    -   Item 2
        -   Item 3
    -   Item 4
-   Item 4
    -   Item 5
```

### Ordered List

Ordered lists MUST be numbered sequentially starting with one.

### Consistently Indent List Items

Nested lists MUST be indented by four spaces. List items at the same level MUST be indented consistently.

**Example**:

```markdown
-   Item 1
    -   Nested Item 1
    -   Nested Item 2
    -   Nested Item 3
```

## No Trailing Whitepsace

Lines MUST NOT have trailing spaces, tabs, or Unicode Zs spaces at the end. Trailing spaces MUST NOT be used to create line breaks. If a manual line break is required, the `<br />` tag MAY be used.

_Note_: Trailing space is allowed in indented and fenced code blocks because some languages require it.

## Use Spaces for Indentation

Four spaces MUST be used for indentation. Tabs MUST NOT be used for indentation outside of Code Blocks. Indentation in Code Blocks is treated verbatim once block indentation has been stripped.

## Use One Consecutive Blank Line as a Block Separator

One, and only one, blank line MUST be used to separate blocks.

## Line Length

Because all modern tools support automatic line wrapping, line length is not enforced. Lines MAY be broken by a single _Line Feed_ character.

## Block Quotes

There MUST be one space after the block quote marker ("&lt;"). When nesting block quotes the space after each except the last MAY be omitted. Block quotes MUST not have blank lines inside the block.

## Code Blocks

Code blocks MUST be preceeded and followed by one blank line and MUST be fenced. Indented code blocks MUST NOT be used. Both the grave ("&grave;") and tilde ("&tilde;") style fences MAY be used. The opening and closing fences MUST be the same marker, MUST be at least three marker characters, and MUST be of the same length.

Code Blocks MAY be indented; when doing so all lines of the block SHOULD be indented similarly. When rendering, the leading block indentation will be stripped from the code.

Code Blocks MUST have a langauge specifier immediately after the opening fence. For plain text, use the `text` language marker.

## Inline HTML

Only the following inline HTML tags are permitted:

| Tag          | Use                                                                                              |
| :----------: | ------------------------------------------------------------------------------------------------ |
|     `img`    | As an alternative when more control is required, e.g., setting the width and height of the image |
|      `a`     | For named references (`#name`) or when the additional control is required                        |
|      `u`     | Underline text                                                                                   |
| `sup`, `sub` | Superscript and subscript text                                                                   |
|    `mark`    | Highlighted text                                                                                 |
|     `del`    | Strikethrough (deleted) text                                                                     |
|    `small`   | Smaller text                                                                                     |
|     `br`     | Inserting a manual line break                                                                    |

## Horizontal Divider

To add an Horizontal Divider use three "&dash;" characters.

**Example**:

```markdown
---
```

## Images Have `alt` Text

All images MUST have alternate text included.

**Example**:

```markdown
![Alternate text](image.jpg)
```

**Or with HTML as**:

```html
<img src="image.jpg" alt="Alternate text" />
```

## Files End with a Single Line Feed Character

All Markdown files MUST end with a single _Line Feed_ character.

## Text Styles

Only the following text style markers MAY be used:

| Marker | Meaning |
| :---: | --- |
| `_` | Emphasis (Italic) |
| `**` | Strong (Bold) |
| `~~` | Strikethrough |

Other styles MAY use the inline HTML tags.

## Tables

Table rows MUST have both the leading and trailing _Vertical Bar_ (Pipe) character.

**Example**:

```markdown
| Header | Header |
| ------ | ------ |
| Cell   | Cell   |
```
