---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /fr/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
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
# Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode rend le document en image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Définissez la propriété "TiffCompression" sur "TiffCompression.None" pour ne pas appliquer de compression lors de l'enregistrement,
# ce qui peut entraîner un fichier de sortie très volumineux.
# Définissez la propriété "TiffCompression" sur "TiffCompression.Rle" pour appliquer la compression RLE
# Définissez la propriété "TiffCompression" sur "TiffCompression.Lzw" pour appliquer la compression LZW.
# Définissez la propriété "TiffCompression" sur "TiffCompression.Ccitt3" pour appliquer la compression CCITT3.
# Définissez la propriété "TiffCompression" sur "TiffCompression.Ccitt4" pour appliquer la compression CCITT4.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

