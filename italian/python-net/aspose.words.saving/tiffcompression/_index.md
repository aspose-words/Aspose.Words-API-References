---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /it/python-net/aspose.words.saving/tiffcompression/
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
# Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo rende il documento in un'immagine.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Imposta la proprietà "TiffCompression" su "TiffCompression.None" per non applicare compressione durante il salvataggio,
# il che può risultare in un file di output molto grande.
# Imposta la proprietà "TiffCompression" su "TiffCompression.Rle" per applicare la compressione RLE
# Imposta la proprietà "TiffCompression" su "TiffCompression.Lzw" per applicare la compressione LZW.
# Imposta la proprietà "TiffCompression" su "TiffCompression.Ccitt3" per applicare la compressione CCITT3.
# Imposta la proprietà "TiffCompression" su "TiffCompression.Ccitt4" per applicare la compressione CCITT4.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

