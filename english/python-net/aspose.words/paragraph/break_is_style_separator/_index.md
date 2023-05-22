---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_table_of_contents("\\o \\h \\z \\u")
builder.insert_break(aw.BreakType.PAGE_BREAK)

# Insert a paragraph with a style that the TOC will pick up as an entry.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1

# Both these strings are in the same paragraph and will therefore show up on the same TOC entry.
builder.write("Heading 1. ")
builder.write("Will appear in the TOC. ")

# If we insert a style separator, we can write more text in the same paragraph
# and use a different style without showing up in the TOC.
# If we use a heading type style after the separator, we can draw multiple TOC entries from one document text line.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")

self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Paragraph.break_is_style_separator.docx")
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

