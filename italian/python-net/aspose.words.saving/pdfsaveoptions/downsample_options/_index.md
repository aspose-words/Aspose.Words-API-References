---
title: PdfSaveOptions.downsample_options property
linktitle: downsample_options property
articleTitle: downsample_options property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.downsample_options property. Allows to specify downsample options."
type: docs
weight: 110
url: /it/python-net/aspose.words.saving/pdfsaveoptions/downsample_options/
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
* class [PdfSaveOptions](../)

