---
title: PdfSaveOptions.zoom_factor property
linktitle: zoom_factor property
articleTitle: zoom_factor property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.zoom_factor property. Gets or sets a value determining zoom factor (in percentages) for a document."
type: docs
weight: 380
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/zoom_factor/
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

