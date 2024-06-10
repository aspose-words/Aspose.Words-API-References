---
title: LayoutOptions.comment_display_mode property
linktitle: comment_display_mode property
articleTitle: comment_display_mode property
second_title: Aspose.Words for Python
description: "LayoutOptions.comment_display_mode property. Gets or sets the way comments are rendered"
type: docs
weight: 30
url: /python-net/aspose.words.layout/layoutoptions/comment_display_mode/
---

## LayoutOptions.comment_display_mode property

Gets or sets the way comments are rendered.
Default value is [CommentDisplayMode.SHOW_IN_BALLOONS](../../commentdisplaymode/#SHOW_IN_BALLOONS).



```python
@property
def comment_display_mode(self) -> aspose.words.layout.CommentDisplayMode:
    ...

@comment_display_mode.setter
def comment_display_mode(self, value: aspose.words.layout.CommentDisplayMode):
    ...

```

### Remarks

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW_IN_ANNOTATIONS](../../commentdisplaymode/#SHOW_IN_ANNOTATIONS).



### Examples

Shows how to show comments when saving a document to a rendered format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'J.D.', datetime.now())
comment.set_text('My comment.')
builder.current_paragraph.append_child(comment)
# SHOW_IN_ANNOTATIONS is only available in Pdf1.7 and Pdf1.5 formats.
# In other formats, it will work similarly to Hide.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_ANNOTATIONS
doc.save(ARTIFACTS_DIR + 'Document.show_comments_in_annotations.pdf')
# Note that it's required to rebuild the document page layout (via Document.update_page_layout() method)
# after changing the "Document.layout_options" values.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_BALLOONS
doc.update_page_layout()
doc.save(ARTIFACTS_DIR + 'Document.show_comments_in_balloons.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

