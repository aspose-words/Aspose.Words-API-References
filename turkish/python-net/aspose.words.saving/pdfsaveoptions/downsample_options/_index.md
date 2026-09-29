---
title: PdfSaveOptions.downsample_options property
linktitle: downsample_options property
articleTitle: downsample_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.downsample_options property. Allows to specify downsample options."
type: docs
weight: 110
url: /tr/python-net/aspose.words.saving/pdfsaveoptions/downsample_options/
---

## PdfSaveOptions.downsample_options property

Allows to specify downsample options.


```python
@property
def downsample_options(self) -> aspose.words.saving.DownsampleOptions:
    ...

@downsample_options.setter
def downsample_options(self, value: aspose.words.saving.DownsampleOptions):
    ...

```

### Examples

Shows how to change the resolution of images in the PDF document.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# Varsayılan olarak, Aspose.Words PDF olarak kaydettiğimiz bir belgedeki tüm görüntüleri 220 ppi'ye düşürür.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# \"Resolution\" özelliğini \"36\" olarak ayarlayın, tüm görüntüleri 36 ppi'ye düşürmek için.
options.downsample_options.resolution = 36
# \"ResolutionThreshold\" özelliğini yalnızca aşağıdaki durumlarda düşürme uygulamak için ayarlayın
# çözünürlüğü 128 ppi'den yüksek olan görüntülere.
options.downsample_options.resolution_threshold = 128
# Bu aşamada, belgeden yalnızca ilk iki görüntü düşürülecek.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

