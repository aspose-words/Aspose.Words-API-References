---
title: ParagraphFormat.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "ParagraphFormat.style_identifier property. Gets or sets the locale independent style identifier of the paragraph style applied to this formatting."
type: docs
weight: 350
url: /python-net/aspose.words/paragraphformat/style_identifier/
---

## ParagraphFormat.style_identifier property

Gets or sets the locale independent style identifier of the paragraph style applied to this formatting.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a table of contents for the first page of the document.
# Configure the table to pick up paragraphs with headings of levels 1 to 3.
# Also, set its entries to be hyperlinks that will take us
# to the location of the heading when left-clicked in Microsoft Word.
builder.insert_table_of_contents("\\o \"1-3\" \\h \\z \\u")
builder.insert_break(aw.BreakType.PAGE_BREAK)

# Populate the table of contents by adding paragraphs with heading styles.
# Each such heading with a level between 1 and 3 will create an entry in the table.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 1.1")
builder.writeln("Heading 1.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("Heading 2")
builder.writeln("Heading 3")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 3.1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln("Heading 3.1.1")
builder.writeln("Heading 3.1.2")
builder.writeln("Heading 3.1.3")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln("Heading 3.1.3.1")
builder.writeln("Heading 3.1.3.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln("Heading 3.2")
builder.writeln("Heading 3.3")

# A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.update_fields()
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_toc.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

