---
title: CommentDisplayMode enumeration
linktitle: CommentDisplayMode enumeration
articleTitle: CommentDisplayMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.CommentDisplayMode enumeration. Specifies the rendering mode for document comments."
type: docs
weight: 10
url: /ru/python-net/aspose.words.layout/commentdisplaymode/
---

## CommentDisplayMode enumeration

Specifies the rendering mode for document comments.


### Members

| Name | Description |
| --- | --- |
| HIDE | No document comments are rendered. |
| SHOW_IN_BALLOONS | Renders document comments in balloons in the margin. This is the default value. |
| SHOW_IN_ANNOTATIONS | Renders document comments in annotations. This is only available for Pdf format. |

### Examples

Shows how to show comments when saving a document to a rendered format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
builder.current_paragraph.append_child(comment)
# ShowInAnnotations доступен только в форматах Pdf1.7 и Pdf1.5.
# В других форматах он будет работать аналогично Hide.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_ANNOTATIONS
doc.save(file_name=ARTIFACTS_DIR + 'Document.ShowCommentsInAnnotations.pdf')
# Обратите внимание, что требуется перестроить макет страниц документа (через метод Document.UpdatePageLayout()).
# после изменения значений Document.LayoutOptions.
doc.layout_options.comment_display_mode = aw.layout.CommentDisplayMode.SHOW_IN_BALLOONS
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.ShowCommentsInBalloons.pdf')
```

### See Also

* module [aspose.words.layout](../)

