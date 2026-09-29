---
title: DownsampleOptions.resolution_threshold property
linktitle: resolution_threshold property
articleTitle: resolution_threshold property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution_threshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /es/python-net/aspose.words.saving/downsampleoptions/resolution_threshold/
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
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Por defecto, Aspose.Words reduce la resolución de todas las imágenes en un documento que guardamos en PDF a 220 ppp.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Establezca la propiedad "Resolution" a "36" para reducir la resolución de todas las imágenes a 36 ppp.
options.downsample_options.resolution = 36
# Establezca la propiedad "ResolutionThreshold" para aplicar la reducción de resolución solo a
# imágenes con una resolución superior a 128 ppp.
options.downsample_options.resolution_threshold = 128
# Solo las dos primeras imágenes del documento se reducirán en este paso.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

