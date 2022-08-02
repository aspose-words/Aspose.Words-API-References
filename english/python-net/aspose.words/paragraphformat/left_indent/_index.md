---
title: left_indent property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the value (in points) that represents the left indent for paragraph."
type: docs
weight: 170
url: /python-net/aspose.words/paragraphformat/left_indent/
---

## ParagraphFormat.left_indent property

Gets or sets the value (in points) that represents the left indent for paragraph.


### Examples

Shows how to configure paragraph formatting to create off-center text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Center all text that the document builder writes, and set up indents.
# The indent configuration below will create a body of text that will sit asymmetrically on the page.
# The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
paragraph_format = builder.paragraph_format
paragraph_format.alignment = aw.ParagraphAlignment.CENTER
paragraph_format.left_indent = 100
paragraph_format.right_indent = 50
paragraph_format.space_after = 25

builder.writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.")
builder.writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.set_paragraph_formatting.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

