---
title: RevisionOptions.show_revision_bars property
linktitle: show_revision_bars property
articleTitle: show_revision_bars property
second_title: Aspose.Words for Python
description: "RevisionOptions.show_revision_bars property. Allows to specify whether revision bars should be rendered near lines containing revised content"
type: docs
weight: 200
url: /ru/python-net/aspose.words.layout/revisionoptions/show_revision_bars/
---

## RevisionOptions.show_revision_bars property

Allows to specify whether revision bars should be rendered near lines containing revised content.
Default value is ``True``.



```python
@property
def show_revision_bars(self) -> bool:
    ...

@show_revision_bars.setter
def show_revision_bars(self, value: bool):
    ...

```

### Examples

Shows how to alter the appearance of revisions in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте правку, затем измените цвет всех правок на зелёный.
builder.writeln('This is not a revision.')
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('This is a revision.')
doc.stop_track_revisions()
builder.writeln('This is not a revision.')
# Удалите полосу, которая появляется слева от каждой исправленной строки.
doc.layout_options.revision_options.inserted_text_color = aw.layout.RevisionColor.BRIGHT_GREEN
doc.layout_options.revision_options.show_revision_bars = False
doc.layout_options.revision_options.revision_bars_position = aw.drawing.HorizontalAlignment.RIGHT
doc.save(file_name=ARTIFACTS_DIR + 'Revision.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

