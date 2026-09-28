---
title: PdfSaveOptions.zoom_factor property
linktitle: zoom_factor property
articleTitle: zoom_factor property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_factor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 380
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
---

## PdfSaveOptions.zoom_factor property

Gets or sets a value determining zoom factor (in percentages) for a document.


```python
@property
def zoom_factor(self) -> int:
    ...

@zoom_factor.setter
def zoom_factor(self, value: int):
    ...

```

### Remarks

This value is used only if [PdfSaveOptions.zoom_behavior](../zoom_behavior/) is set to [PdfZoomBehavior.ZOOM_FACTOR](../../pdfzoombehavior/#ZOOM_FACTOR).



### Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
# قم بتعيين الخاصية "ZoomBehavior" إلى "PdfZoomBehavior.ZoomFactor" لجعل قارئ PDF
# يطبق عامل تكبير يعتمد على النسبة المئوية عند فتح المستند به.
# قم بتعيين الخاصية "ZoomFactor" إلى "25" لإعطاء عامل التكبير قيمة 25٪.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# عند فتح هذا المستند باستخدام قارئ مثل Adobe Acrobat، سنرى المستند مُقاسًا إلى ربع حجمه الفعلي.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

