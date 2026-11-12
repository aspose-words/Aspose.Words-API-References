---
title: DownsampleOptions.downsample_images property
linktitle: downsample_images property
articleTitle: downsample_images property
second_title: Aspose.Words for Python
description: "DownsampleOptions.downsample_images property. Specifies whether images should be downsampled."
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/downsampleoptions/downsample_images/
---

## DownsampleOptions.downsample_images property

Specifies whether images should be downsampled.


```python
@property
def downsample_images(self) -> bool:
    ...

@downsample_images.setter
def downsample_images(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.



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

