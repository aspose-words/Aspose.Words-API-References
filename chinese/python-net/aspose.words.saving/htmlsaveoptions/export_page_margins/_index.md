---
title: HtmlSaveOptions.export_page_margins property
linktitle: export_page_margins property
articleTitle: export_page_margins property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_page_margins property. Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 210
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/export_page_margins/
---

## HtmlSaveOptions.export_page_margins property

Specifies whether page margins is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_page_margins(self) -> bool:
    ...

@export_page_margins.setter
def export_page_margins(self, value: bool):
    ...

```

### Remarks

Aspose.Words does not show area of page margins by default.
If any elements are completely or partially clipped by the document edge the displayed area can be extended with
this option.


### Examples

Shows how to show out-of-bounds objects in output HTML documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用构建器插入一个没有换行的形状。
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=200, height=200)
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.wrap_type = aw.drawing.WrapType.NONE
# 负的形状位置值可能会将形状放置在页面边界之外。
# 如果我们将其导出为 HTML，形状将会被截断。
shape.left = -150
# 将文档保存为 HTML 时，我们可以传入 SaveOptions 对象
# 决定是否调整页面以完整显示超出边界的对象。
# 如果我们将 \"ExportPageMargins\" 标志设置为 \"true\"，形状将在输出的 HTML 中完整可见。
# 如果我们将 \"ExportPageMargins\" 标志设置为 \"false\"，
# 我们的文档将会像在 Microsoft Word 中看到的那样显示被截断的形状。
options = aw.saving.HtmlSaveOptions()
options.export_page_margins = export_page_margins
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageMargins.html')
if export_page_margins:
    self.assertTrue('<style type="text/css">div.Section_1 { margin:70.85pt }</style>' in out_doc_contents)
    self.assertTrue('<div class="Section_1"><p style="margin-top:0pt; margin-left:150pt; margin-bottom:0pt">' in out_doc_contents)
else:
    self.assertFalse('style type="text/css">' in out_doc_contents)
    self.assertTrue('<div><p style="margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt">' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

