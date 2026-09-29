---
title: DownsampleOptions class
linktitle: DownsampleOptions class
articleTitle: DownsampleOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.DownsampleOptions class. Allows to specify downsample options"
type: docs
weight: 150
url: /es/python-net/aspose.words.saving/downsampleoptions/
---

## DownsampleOptions class

Allows to specify downsample options.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [DownsampleOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [downsample_images](./downsample_images/) | Specifies whether images should be downsampled. |
| [resolution](./resolution/) | Specifies the resolution in pixels per inch which the images should be downsampled to. |
| [resolution_threshold](./resolution_threshold/) | Specifies the threshold resolution in pixels per inch. If resolution of an image in the document is less than threshold value, the downsampling algorithm will not be applied. A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled. |

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

* module [aspose.words.saving](../)

