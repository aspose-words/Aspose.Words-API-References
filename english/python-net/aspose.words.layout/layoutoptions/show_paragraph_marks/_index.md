---
title: LayoutOptions.show_paragraph_marks property
linktitle: show_paragraph_marks property
articleTitle: show_paragraph_marks property
second_title: Aspose.Words for Python
description: "LayoutOptions.show_paragraph_marks property. Gets or sets indication of whether paragraph marks are rendered"
type: docs
weight: 90
url: /python-net/aspose.words.layout/layoutoptions/show_paragraph_marks/
---

## LayoutOptions.show_paragraph_marks property

Gets or sets indication of whether paragraph marks are rendered.
Default is ``False``.



```python
@property
def show_paragraph_marks(self) -> bool:
    ...

@show_paragraph_marks.setter
def show_paragraph_marks(self, value: bool):
    ...

```

### Examples

Shows how to show paragraph marks in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
# with a pilcrow (¶) symbol when we render the document.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
doc.layout_options.show_paragraph_marks = show_paragraph_marks
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsParagraphMarks.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

