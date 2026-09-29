---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /it/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
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

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

