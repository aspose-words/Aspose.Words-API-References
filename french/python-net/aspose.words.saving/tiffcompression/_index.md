---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /fr/python-net/aspose.words.saving/tiffcompression/
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

* module [aspose.words.saving](../)

