---
title: show_revision_bars property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify whether revision bars should be rendered near lines containing revised content"
type: docs
weight: 180
url: /python-net/aspose.words.layout/revisionoptions/show_revision_bars/
---

## RevisionOptions.show_revision_bars property

Allows to specify whether revision bars should be rendered near lines containing revised content.
Default value is True.


### Examples

Shows how to alter the appearance of revisions in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a revision, then change the color of all revisions to green.
builder.writeln("This is not a revision.")
doc.start_track_revisions("John Doe", datetime.now())
builder.writeln("This is a revision.")
doc.stop_track_revisions()
builder.writeln("This is not a revision.")

# Remove the bar that appears to the left of every revised line.
doc.layout_options.revision_options.inserted_text_color = aw.layout.RevisionColor.BRIGHT_GREEN
doc.layout_options.revision_options.show_revision_bars = False

doc.save(ARTIFACTS_DIR + "Document.layout_options_revisions.pdf")
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

