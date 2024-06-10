---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Run 1. ')
# The document builder has a cursor, which acts as the part of the document
# where the builder appends new nodes when we use its document construction methods.
# This cursor functions in the same way as Microsoft Word's blinking cursor,
# and it also always ends up immediately after any node that the builder just inserted.
# To append content to a different part of the document,
# we can move the cursor to a different node with the "MoveTo" method.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# The cursor is now in front of the node that we moved it to.
# Adding a second run will insert it in front of the first run.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Move the cursor to the end of the document to continue appending text to the end as before.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

