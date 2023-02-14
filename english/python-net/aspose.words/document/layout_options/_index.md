---
title: layout_options property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document."
type: docs
weight: 250
url: /python-net/aspose.words/document/layout_options/
---

## Document.layout_options property

Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document.



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

Shows how to hide text in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.writeln("This text is not hidden.")
builder.font.hidden = True
builder.writeln("This text is hidden.")

doc.layout_options.show_hidden_text = show_hidden_text

doc.save(ARTIFACTS_DIR + "Document.layout_options_hidden_text.pdf")
```

Shows how to show paragraph marks in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
# with a pilcrow (¶) symbol when we render the document.
builder.writeln("Hello world!")
builder.writeln("Hello again!")

doc.layout_options.show_paragraph_marks = show_paragraph_marks

doc.save(ARTIFACTS_DIR + "Document.layout_options_paragraph_marks.pdf")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

