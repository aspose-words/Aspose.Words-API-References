---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /es/python-net/aspose.words.saving/tiffcompression/
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
# Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
# para modificar la forma en que ese método renderiza el documento en una imagen.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Establezca la propiedad "TiffCompression" a "TiffCompression.None" para no aplicar compresión al guardar,
# lo que puede resultar en un archivo de salida muy grande.
# Establezca la propiedad "TiffCompression" a "TiffCompression.Rle" para aplicar compresión RLE
# Establezca la propiedad "TiffCompression" a "TiffCompression.Lzw" para aplicar compresión LZW.
# Establezca la propiedad "TiffCompression" a "TiffCompression.Ccitt3" para aplicar compresión CCITT3.
# Establezca la propiedad "TiffCompression" a "TiffCompression.Ccitt4" para aplicar compresión CCITT4.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

