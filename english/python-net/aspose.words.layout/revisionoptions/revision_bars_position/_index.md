---
title: RevisionOptions.revision_bars_position property
linktitle: revision_bars_position property
articleTitle: revision_bars_position property
second_title: Aspose.Words for Python
description: "RevisionOptions.revision_bars_position property. Gets or sets rendering position of revision bars"
type: docs
weight: 140
url: /python-net/aspose.words.layout/revisionoptions/revision_bars_position/
---

## RevisionOptions.revision_bars_position property

Gets or sets rendering position of revision bars.
Default value is [HorizontalAlignment.OUTSIDE](../../../aspose.words.drawing/horizontalalignment/#OUTSIDE).



```python
@property
def revision_bars_position(self) -> aspose.words.drawing.HorizontalAlignment:
    ...

@revision_bars_position.setter
def revision_bars_position(self, value: aspose.words.drawing.HorizontalAlignment):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Values of [HorizontalAlignment.CENTER](../../../aspose.words.drawing/horizontalalignment/#CENTER) and [HorizontalAlignment.INSIDE](../../../aspose.words.drawing/horizontalalignment/#INSIDE)  are not allowed. |

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
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

