---
title: FixedPageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside Html document."
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/fixedpagesaveoptions/jpeg_quality/
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
# Erstellen Sie ein Objekt "ImageSaveOptions", das wir an die "Save"‑Methode des Dokuments übergeben können
# um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Setzen Sie die Eigenschaft "JpegQuality" auf "10", um bei der Dokumenten‑Renderung stärkere Kompression zu verwenden.
# Dies reduziert die Dateigröße des Dokuments, aber das Bild zeigt deutlichere Kompressionsartefakte.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Setzen Sie die Eigenschaft "JpegQuality" auf "100", um bei der Dokumenten‑Renderung schwächere Kompression zu verwenden.
# Dies wird die Qualität des Bildes verbessern, allerdings auf Kosten einer erhöhten Dateigröße.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

