---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /tr/python-net/aspose.words.saving/tiffcompression/
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
# Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun.
# bu yöntemin belgeyi bir görsele nasıl işlediğini değiştirmek için.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# "TiffCompression" özelliğini "TiffCompression.None" olarak ayarlayarak kaydederken sıkıştırma uygulamayın,
# bu, çok büyük bir çıktı dosyasına neden olabilir.
# "TiffCompression" özelliğini "TiffCompression.Rle" olarak ayarlayarak RLE sıkıştırması uygulayın
# "TiffCompression" özelliğini "TiffCompression.Lzw" olarak ayarlayarak LZW sıkıştırması uygulayın.
# "TiffCompression" özelliğini "TiffCompression.Ccitt3" olarak ayarlayarak CCITT3 sıkıştırması uygulayın.
# "TiffCompression" özelliğini "TiffCompression.Ccitt4" olarak ayarlayarak CCITT4 sıkıştırması uygulayın.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

