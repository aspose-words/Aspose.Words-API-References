---
title: DownsampleOptions.resolution_threshold property
linktitle: resolution_threshold property
articleTitle: resolution_threshold property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution_threshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/downsampleoptions/resolution_threshold/
---

## DownsampleOptions.resolution_threshold property

Specifies the threshold resolution in pixels per inch.
If resolution of an image in the document is less than threshold value,
the downsampling algorithm will not be applied.
A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.


```python
@property
def resolution_threshold(self) -> int:
    ...

@resolution_threshold.setter
def resolution_threshold(self, value: int):
    ...

```

### Remarks

The default value is 0.


### Examples

Shows how to change the resolution of images in the PDF document.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# По умолчанию Aspose.Words уменьшает разрешение всех изображений в документе, сохраняемом в PDF, до 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Установите свойство "Resolution" в "36", чтобы уменьшить разрешение всех изображений до 36 ppi.
options.downsample_options.resolution = 36
# Установите свойство "ResolutionThreshold", чтобы применять уменьшение разрешения только к
# изображениям с разрешением выше 128 ppi.
options.downsample_options.resolution_threshold = 128
# На этом этапе будет уменьшено разрешение только первых двух изображений из документа.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

