---
title: HtmlSaveOptions.export_page_margins property
linktitle: export_page_margins property
articleTitle: export_page_margins property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_page_margins property. Specifies whether page margins is exported to HTML, MHTML or EPUB"
type: docs
weight: 210
url: /ar/python-net/aspose.words.saving/htmlsaveoptions/export_page_margins/
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
# استخدم مُنشئًا لإدراج شكل بدون تغليف.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=200, height=200)
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.wrap_type = aw.drawing.WrapType.NONE
# قد تؤدي قيم موضع الشكل السالبة إلى وضع الشكل خارج حدود الصفحة.
# إذا صدّرنا هذا إلى HTML، سيظهر الشكل مقطوعًا.
shape.left = -150
# عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
# لتحديد ما إذا كان يجب تعديل الصفحة لعرض الكائنات الخارجة عن الحدود بالكامل.
# إذا ضبطنا علامة "ExportPageMargins" إلى "true"، سيكون الشكل مرئيًا بالكامل في HTML الناتج.
# إذا ضبطنا علامة "ExportPageMargins" إلى "false",
# ستعرض مستندنا الشكل مقطوعًا كما نراه في Microsoft Word.
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

