---
title: ImageSaveOptions.image_color_mode property
linktitle: image_color_mode property
articleTitle: image_color_mode property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_color_mode property. Gets or sets the color mode for the generated images."
type: docs
weight: 40
url: /tr/python-net/aspose.words.saving/imagesaveoptions/image_color_mode/
---

## ImageSaveOptions.image_color_mode property

Gets or sets the color mode for the generated images.


```python
@property
def image_color_mode(self) -> aspose.words.saving.ImageColorMode:
    ...

@image_color_mode.setter
def image_color_mode(self, value: aspose.words.saving.ImageColorMode):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is [ImageColorMode.NONE](../../imagecolormode/#NONE).




### Examples

Shows how to set a color mode when rendering documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Belgeyi bir görüntü olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
# kaydetme işleminin oluşturacağı görüntü için bir renk modu seçin.
# "ImageColorMode" özelliğini "ImageColorMode.BlackAndWhite" olarak ayarlarsak,
# kaydetme işlemi belgeyi işlerken gri tonlamalı renk azaltımı uygulayacaktır.
# "ImageColorMode" özelliğini "ImageColorMode.Grayscale" olarak ayarlarsak,
# kaydetme işlemi belgeyi tek renkli bir görüntüye dönüştürecektir.
# Eğer "ImageColorMode" özelliğini "None" olarak ayarlarsak, kaydetme işlemi varsayılan yöntemi uygulayacaktır
# ve çıktı görüntüsünde belgenin tüm renklerini korur.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

