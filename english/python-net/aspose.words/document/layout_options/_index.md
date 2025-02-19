﻿---
title: Document.layout_options property
linktitle: layout_options property
articleTitle: layout_options property
second_title: Aspose.Words for Python
description: "Document.layout_options property. Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document."
type: docs
weight: 260
url: /python-net/aspose.words/document/layout_options/
---

## Document.layout_options property

Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document.



```python
@property
def layout_options(self) -> aspose.words.layout.LayoutOptions:
    ...

```

### Examples

Shows how to hide text in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.writeln('This text is not hidden.')
builder.font.hidden = True
builder.writeln('This text is hidden.')
doc.layout_options.show_hidden_text = show_hidden_text
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsHiddenText.pdf')
```

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

Shows how to alter the appearance of revisions in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a revision, then change the color of all revisions to green.
builder.writeln('This is not a revision.')
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('This is a revision.')
doc.stop_track_revisions()
builder.writeln('This is not a revision.')
# Remove the bar that appears to the left of every revised line.
doc.layout_options.revision_options.inserted_text_color = aw.layout.RevisionColor.BRIGHT_GREEN
doc.layout_options.revision_options.show_revision_bars = False
doc.layout_options.revision_options.revision_bars_position = aw.drawing.HorizontalAlignment.RIGHT
doc.save(file_name=ARTIFACTS_DIR + 'Revision.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

