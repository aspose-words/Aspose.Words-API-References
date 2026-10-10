---
title: PdfSaveOptions.preblend_images property
linktitle: preblend_images property
articleTitle: preblend_images property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.preblend_images property. Gets or sets a value determining whether or not to preblend transparent images with black background color."
type: docs
weight: 290
url: /de/python-net/aspose.words.saving/pdfsaveoptions/preblend_images/
---

## PdfSaveOptions.preblend_images property

Gets or sets a value determining whether or not to preblend transparent images with black background color.


```python
@property
def preblend_images(self) -> bool:
    ...

@preblend_images.setter
def preblend_images(self, value: bool):
    ...

```

### Remarks

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary.
Also preblending images may decrease PDF rendering performance.

The default value is ``False``.




### Examples

Shows how to preblend images with transparent backgrounds while saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "PreblendImages" auf "true", um transparente Bilder vorzublenden
# mit einem Hintergrund, was Artefakte reduzieren kann.
# Setzen Sie die Eigenschaft "PreblendImages" auf "false", um transparente Bilder normal darzustellen.
options.preblend_images = preblend_images
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PreblendImages.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

