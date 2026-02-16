---
title: LayoutOptions.revision_options property
linktitle: revision_options property
articleTitle: revision_options property
second_title: Aspose.Words for Python
description: "LayoutOptions.revision_options property. Gets revision options."
type: docs
weight: 80
url: /python-net/aspose.words.layout/layoutoptions/revision_options/
---

## LayoutOptions.revision_options property

Gets revision options.


```python
@property
def revision_options(self) -> aspose.words.layout.RevisionOptions:
    ...

```

### Examples

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

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

