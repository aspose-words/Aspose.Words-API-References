---
title: RevisionOptions.inserted_text_color property
linktitle: inserted_text_color property
articleTitle: inserted_text_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.inserted_text_color property. Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION)"
type: docs
weight: 60
url: /python-net/aspose.words.layout/revisionoptions/inserted_text_color/
---

## RevisionOptions.inserted_text_color property

Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION).
Default value is [RevisionColor.BY_AUTHOR](../../revisioncolor/#BY_AUTHOR).



```python
@property
def inserted_text_color(self) -> aspose.words.layout.RevisionColor:
    ...

@inserted_text_color.setter
def inserted_text_color(self, value: aspose.words.layout.RevisionColor):
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
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

