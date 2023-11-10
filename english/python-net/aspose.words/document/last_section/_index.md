---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 240
url: /python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()

# A blank document contains one section by default,
# which contains child nodes that we can edit.
self.assertEqual(1, doc.sections.count)

# Use a document builder to add text to the first section.
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Create a second section by inserting a section break.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)

self.assertEqual(2, doc.sections.count)

# Each section has its own page setup settings.
# We can split the text in the second section into two columns.
# This will not affect the text in the first section.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln("Column 1.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln("Column 2.")

self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)

doc.save(ARTIFACTS_DIR + "Section.first_and_last.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

