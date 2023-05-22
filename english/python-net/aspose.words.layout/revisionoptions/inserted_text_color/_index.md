---
title: RevisionOptions.inserted_text_color property
linktitle: inserted_text_color property
articleTitle: inserted_text_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.inserted_text_color property. Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION)"
type: docs
weight: 40
url: /python-net/aspose.words.layout/revisionoptions/inserted_text_color/
---

## RevisionOptions.inserted_text_color property

Allows to specify the color to be used for inserted content [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION).
Default value is [RevisionColor.BY_AUTHOR](../../revisioncolor/#BY_AUTHOR).



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

