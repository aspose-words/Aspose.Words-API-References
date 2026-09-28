---
title: DownsampleOptions.resolution property
linktitle: resolution property
articleTitle: resolution property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution property. Specifies the resolution in pixels per inch which the images should be downsampled to."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/downsampleoptions/resolution/
---

## DownsampleOptions.resolution property

Specifies the resolution in pixels per inch which the images should be downsampled to.


```python
@property
def resolution(self) -> int:
    ...

@resolution.setter
def resolution(self, value: int):
    ...

```

### Remarks

The default value is 220 ppi.


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

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

