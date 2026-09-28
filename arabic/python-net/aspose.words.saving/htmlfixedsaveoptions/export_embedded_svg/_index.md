---
title: HtmlFixedSaveOptions.export_embedded_svg property
linktitle: export_embedded_svg property
articleTitle: export_embedded_svg property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_svg property. Specifies whether SVG resources should be embedded into Html document"
type: docs
weight: 70
url: /ar/python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_svg/
---

## HtmlFixedSaveOptions.export_embedded_svg property

Specifies whether SVG resources should be embedded into Html document.
Default value is ``True``.



```python
@property
def export_embedded_svg(self) -> bool:
    ...

@export_embedded_svg.setter
def export_embedded_svg(self, value: bool):
    ...

```

### Examples

Shows how to determine where to store SVG objects when exporting a document to Html.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# عند تصدير مستند يحتوي على كائنات SVG إلى .html،
# يمكن لـ Aspose.Words وضع هذه الكائنات في موقعين محتملين.
# ضبط العلامة "ExportEmbeddedSvg" إلى "true" سيضمّن جميع البيانات الخام لكائنات SVG
# داخل HTML الناتج، داخل وسوم <image>.
# ضبط هذه العلامة إلى "false" سيُنشئ ملفًا في نظام الملفات المحلي لكل كائن SVG.
# سيرتبط HTML بكل ملف باستخدام السمة "data" لوسم <object>.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_svg = export_svgs
doc.save(file_name=ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedSvgs.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedSvgs.html')
if export_svgs:
    self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg'))
    self.assertTrue(re.compile('<image id=\\"image004\\" xlink:href=.+/>').search(out_doc_contents) is not None)
else:
    self.assertTrue(system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg'))
    self.assertTrue(re.compile('<object type=\\"image/svg\\+xml\\" data=\\"HtmlFixedSaveOptions\\.ExportEmbeddedSvgs/svg001\\.svg\\"></object>').search(out_doc_contents) is not None)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

