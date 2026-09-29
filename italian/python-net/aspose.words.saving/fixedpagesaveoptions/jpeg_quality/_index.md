---
title: FixedPageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside Html document."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/fixedpagesaveoptions/jpeg_quality/
---

## FixedPageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the JPEG images inside Html document.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo rende il documento in un'immagine.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Imposta la proprietà "JpegQuality" a "10" per usare una compressione più forte durante il rendering del documento.
# Ciò ridurrà la dimensione del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Imposta la proprietà "JpegQuality" a "100" per usare una compressione più debole durante il rendering del documento.
# Questo migliorerà la qualità dell'immagine a costo di un aumento delle dimensioni del file.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

