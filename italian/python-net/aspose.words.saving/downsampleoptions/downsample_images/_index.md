---
title: DownsampleOptions.downsample_images property
linktitle: downsample_images property
articleTitle: downsample_images property
second_title: Aspose.Words for Python
description: "DownsampleOptions.downsample_images property. Specifies whether images should be downsampled."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/downsampleoptions/downsample_images/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Per impostazione predefinita, Aspose.Words riduce la risoluzione di tutte le immagini in un documento che salviamo in PDF a 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Imposta la proprietà "Resolution" a "36" per ridurre la risoluzione di tutte le immagini a 36 ppi.
options.downsample_options.resolution = 36
# Imposta la proprietà "ResolutionThreshold" per applicare la riduzione della risoluzione solo a
# immagini con una risoluzione superiore a 128 ppi.
options.downsample_options.resolution_threshold = 128
# Solo le prime due immagini del documento saranno ridotte a questa fase.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

