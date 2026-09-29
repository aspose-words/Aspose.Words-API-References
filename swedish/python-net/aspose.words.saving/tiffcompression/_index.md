---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /sv/python-net/aspose.words.saving/tiffcompression/
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
# Skapa ett "ImageSaveOptions"‑objekt som vi kan skicka till dokumentets "Save"‑metod
# för att ändra hur den metoden renderar dokumentet till en bild.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Ställ in egenskapen "TiffCompression" till "TiffCompression.None" för att inte använda någon komprimering vid sparning,
# vilket kan resultera i en mycket stor utdatafil.
# Ställ in egenskapen "TiffCompression" till "TiffCompression.Rle" för att tillämpa RLE-komprimering
# Ställ in egenskapen "TiffCompression" till "TiffCompression.Lzw" för att tillämpa LZW-komprimering.
# Ställ in egenskapen "TiffCompression" till "TiffCompression.Ccitt3" för att tillämpa CCITT3-komprimering.
# Ställ in egenskapen "TiffCompression" till "TiffCompression.Ccitt4" för att tillämpa CCITT4-komprimering.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

