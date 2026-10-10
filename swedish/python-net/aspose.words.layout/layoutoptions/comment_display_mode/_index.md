---
title: LayoutOptions.comment_display_mode property
linktitle: comment_display_mode property
articleTitle: comment_display_mode property
second_title: Aspose.Words for Python
description: "LayoutOptions.comment_display_mode property. Gets or sets the way comments are rendered"
type: docs
weight: 30
url: /sv/python-net/aspose.words.layout/layoutoptions/comment_display_mode/
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
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
builder.current_paragraph.append_child(comment)
# ShowInAnnotations är endast tillgänglig i Pdf1.7‑ och Pdf1.5‑format.
# I andra format kommer den att fungera på liknande sätt som Hide.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_ANNOTATIONS
doc.save(file_name=ARTIFACTS_DIR + 'Document.ShowCommentsInAnnotations.pdf')
# Observera att det krävs att bygga om dokumentets sidlayout (via metoden Document.UpdatePageLayout())
# efter att ha ändrat värdena i Document.LayoutOptions.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_BALLOONS
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.ShowCommentsInBalloons.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

