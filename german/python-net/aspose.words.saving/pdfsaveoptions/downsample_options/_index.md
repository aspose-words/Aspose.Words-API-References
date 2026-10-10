---
title: PdfSaveOptions.downsample_options property
linktitle: downsample_options property
articleTitle: downsample_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.downsample_options property. Allows to specify downsample options."
type: docs
weight: 110
url: /de/python-net/aspose.words.saving/pdfsaveoptions/downsample_options/
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
* class [PdfSaveOptions](../)

