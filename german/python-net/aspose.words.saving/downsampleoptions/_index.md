---
title: DownsampleOptions class
linktitle: DownsampleOptions class
articleTitle: DownsampleOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.DownsampleOptions class. Allows to specify downsample options"
type: docs
weight: 150
url: /de/python-net/aspose.words.saving/downsampleoptions/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Standardmäßig reduziert Aspose.Words die Auflösung aller Bilder in einem Dokument, das wir als PDF speichern, auf 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Setzen Sie die Eigenschaft "Resolution" auf "36", um alle Bilder auf 36 ppi herunterzusampeln.
options.downsample_options.resolution = 36
# Setzen Sie die Eigenschaft "ResolutionThreshold" so, dass die Heruntersampling‑Funktion nur angewendet wird
# auf Bilder mit einer Auflösung über 128 ppi.
options.downsample_options.resolution_threshold = 128
# Nur die ersten beiden Bilder des Dokuments werden in diesem Schritt heruntergesampelt.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

