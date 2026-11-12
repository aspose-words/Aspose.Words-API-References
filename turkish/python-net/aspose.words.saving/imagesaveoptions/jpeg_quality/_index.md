---
title: ImageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the generated JPEG images."
type: docs
weight: 70
url: /tr/python-net/aspose.words.saving/imagesaveoptions/jpeg_quality/
---

## ImageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the generated JPEG images.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Belgenin "Save" yöntemine geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun.
# bu yöntemin belgeyi bir görsele nasıl işlediğini değiştirmek için.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# "JpegQuality" özelliğini "10" olarak ayarlayın, belgeyi işlerken daha güçlü sıkıştırma kullanmak için.
# Bu, belgenin dosya boyutunu azaltacak, ancak görsel daha belirgin sıkıştırma artefaktları gösterecektir.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# "JpegQuality" özelliğini "100" olarak ayarlayın, belgeyi işlerken daha zayıf sıkıştırma kullanmak için.
# Bu, dosya boyutunun artması karşılığında görüntünün kalitesini artıracaktır.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

