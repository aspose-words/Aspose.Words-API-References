---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /es/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
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

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

