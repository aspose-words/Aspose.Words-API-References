---
title: LayoutOptions class
linktitle: LayoutOptions class
articleTitle: LayoutOptions class
second_title: Aspose.Words for Python
description: "aspose.words.layout.LayoutOptions class. Holds the options that allow controlling the document layout process"
type: docs
weight: 70
url: /python-net/aspose.words.layout/layoutoptions/
---

## LayoutOptions class

Holds the options that allow controlling the document layout process.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/python-net/converting-to-fixed-page-format/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [Document.layout_options](../../aspose.words/document/layout_options/) property to access layout options for this document.


Note that after changing any of the options present in this class, [Document.update_page_layout()](../../aspose.words/document/update_page_layout/#default) method
should be called in order for the changed options to be applied to the layout.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [callback](./callback/) | Gets or sets [IPageLayoutCallback](../ipagelayoutcallback/) implementation used by page layout model. |
| [comment_display_mode](./comment_display_mode/) | Gets or sets the way comments are rendered. Default value is [CommentDisplayMode.SHOW_IN_BALLOONS](../commentdisplaymode/#SHOW_IN_BALLOONS). |
| [continuous_section_page_numbering_restart](./continuous_section_page_numbering_restart/) | Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [ignore_printer_metrics](./ignore_printer_metrics/) | Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is ``True``. |
| [keep_original_font_metrics](./keep_original_font_metrics/) | Gets or sets an indication of whether the original font metrics should be used after font substitution. Default is ``True``. |
| [revision_options](./revision_options/) | Gets revision options. |
| [show_hidden_text](./show_hidden_text/) | Gets or sets indication of whether hidden text in the document is rendered. Default is ``False``. |
| [show_paragraph_marks](./show_paragraph_marks/) | Gets or sets indication of whether paragraph marks are rendered. Default is ``False``. |
| [text_shaper_factory](./text_shaper_factory/) | Gets or sets Aspose.Words.Shaping.ITextShaperFactory implementation used for Advanced Typography rendering features. |

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
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words.layout](../)

