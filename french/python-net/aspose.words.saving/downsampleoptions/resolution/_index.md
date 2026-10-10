---
title: DownsampleOptions.resolution property
linktitle: resolution property
articleTitle: resolution property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution property. Specifies the resolution in pixels per inch which the images should be downsampled to."
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/downsampleoptions/resolution/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Par défaut, Aspose.Words réduit la résolution de toutes les images d'un document que nous enregistrons au PDF à 220 ppi.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# Définissez la propriété "Resolution" sur "36" pour réduire la résolution de toutes les images à 36 ppi.
options.downsample_options.resolution = 36
# Définissez la propriété "ResolutionThreshold" pour n'appliquer la réduction de résolution qu'aux
# images dont la résolution est supérieure à 128 ppi.
options.downsample_options.resolution_threshold = 128
# Seules les deux premières images du document seront réduites à ce stade.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

