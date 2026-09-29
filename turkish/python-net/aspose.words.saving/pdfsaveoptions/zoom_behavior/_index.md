---
title: PdfSaveOptions.zoom_behavior property
linktitle: zoom_behavior property
articleTitle: zoom_behavior property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_behavior property. Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer."
type: docs
weight: 370
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/zoom_behavior/
---

## PdfSaveOptions.zoom_behavior property

Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.


```python
@property
def zoom_behavior(self) -> aspose.words.saving.PdfZoomBehavior:
    ...

@zoom_behavior.setter
def zoom_behavior(self, value: aspose.words.saving.PdfZoomBehavior):
    ...

```

### Remarks

The default value is [PdfZoomBehavior.NONE](../../pdfzoombehavior/#NONE), i.e. no fit is applied.



### Examples

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
# \"ZoomBehavior\" özelliğini \"PdfZoomBehavior.ZoomFactor\" olarak ayarlayın, böylece bir PDF okuyucusu
# belgeyi açtığımızda yüzde tabanlı bir yakınlaştırma faktörü uygulasın.
# \"ZoomFactor\" özelliğini \"25\" olarak ayarlayın, böylece yakınlaştırma faktörüne %25 değeri verilir.
options = aw.saving.PdfSaveOptions()
options.zoom_behavior = aw.saving.PdfZoomBehavior.ZOOM_FACTOR
options.zoom_factor = 25
# Adobe Acrobat gibi bir okuyucu kullanarak bu belgeyi açtığımızda, belgenin gerçek boyutunun 1/4'üne ölçeklendiğini göreceğiz.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ZoomBehaviour.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

