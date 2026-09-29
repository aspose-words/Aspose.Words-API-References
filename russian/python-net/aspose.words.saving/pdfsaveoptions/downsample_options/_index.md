---
title: PdfSaveOptions.downsample_options property
linktitle: downsample_options property
articleTitle: downsample_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.downsample_options property. Allows to specify downsample options."
type: docs
weight: 110
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/downsample_options/
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
* class [PdfSaveOptions](../)

