---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /de/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
---

## ImageSaveOptions.tiff_compression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.


```python
@property
def tiff_compression(self) -> aspose.words.saving.TiffCompression:
    ...

@tiff_compression.setter
def tiff_compression(self, value: aspose.words.saving.TiffCompression):
    ...

```

### Remarks

Has effect only when saving to TIFF.

The default value is [TiffCompression.LZW](../../tiffcompression/#LZW).




### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Erstellen Sie ein Objekt "ImageSaveOptions", das wir an die "Save"‑Methode des Dokuments übergeben können
# um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Setzen Sie die "TiffCompression"-Eigenschaft auf "TiffCompression.None", um beim Speichern keine Kompression anzuwenden,
# was zu einer sehr großen Ausgabedatei führen kann.
# Setzen Sie die "TiffCompression"-Eigenschaft auf "TiffCompression.Rle", um RLE-Kompression anzuwenden
# Setzen Sie die "TiffCompression"-Eigenschaft auf "TiffCompression.Lzw", um LZW-Kompression anzuwenden.
# Setzen Sie die "TiffCompression"-Eigenschaft auf "TiffCompression.Ccitt3", um CCITT3-Kompression anzuwenden.
# Setzen Sie die "TiffCompression"-Eigenschaft auf "TiffCompression.Ccitt4", um CCITT4-Kompression anzuwenden.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

