---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /tr/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
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

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

