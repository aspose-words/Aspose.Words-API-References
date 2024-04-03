---
title: ParagraphFormat.page_break_before property
linktitle: page_break_before property
articleTitle: page_break_before property
second_title: Aspose.Words for Python
description: "ParagraphFormat.page_break_before property. True if a page break is forced before the paragraph."
type: docs
weight: 270
url: /python-net/aspose.words/paragraphformat/page_break_before/
---

## ParagraphFormat.page_break_before property

True if a page break is forced before the paragraph.


```python
@property
def page_break_before(self) -> bool:
    ...

@page_break_before.setter
def page_break_before(self, value: bool):
    ...

```

### Examples

Shows how to create paragraphs with page breaks at the beginning.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set this flag to "True" to apply a page break to each paragraph's beginning
# that the document builder will create under this ParagraphFormat configuration.
# The first paragraph will not receive a page break.
# Leave this flag as "False" to start each new paragraph on the same page
# as the previous, provided there is sufficient space.
builder.paragraph_format.page_break_before = page_break_before

builder.writeln("Paragraph 1.")
builder.writeln("Paragraph 2.")

layout_collector = aw.layout.LayoutCollector(doc)
paragraphs = doc.first_section.body.paragraphs

if page_break_before:
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[0]))
    self.assertEqual(2, layout_collector.get_start_page_index(paragraphs[1]))
else:
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[0]))
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[1]))

doc.save(ARTIFACTS_DIR + "ParagraphFormat.page_break_before.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

