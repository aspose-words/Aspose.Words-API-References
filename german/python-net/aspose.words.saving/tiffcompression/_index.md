---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /de/python-net/aspose.words.saving/tiffcompression/
---

## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies no compression. |
| RLE | Specifies the RLE compression scheme. |
| LZW | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| CCITT3 | Specifies the CCITT3 compression scheme. |
| CCITT4 | Specifies the CCITT4 compression scheme. |

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

* module [aspose.words.saving](../)

