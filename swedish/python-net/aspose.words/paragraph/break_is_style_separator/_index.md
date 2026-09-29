---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /sv/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Infoga ett stycke med en stil som TOC kommer att plocka upp som ett post.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# Båda dessa strängar är i samma stycke och kommer därför att visas i samma TOC-post.
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# Om vi infogar en stilseparator kan vi skriva mer text i samma stycke
# och använda en annan stil utan att den visas i innehållsförteckningen.
# Om vi använder en rubriktypstil efter separatorn kan vi skapa flera innehållsförteckningsposter från en dokumenttextrad.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

