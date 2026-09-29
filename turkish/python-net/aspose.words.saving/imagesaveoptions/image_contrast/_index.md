---
title: ImageSaveOptions.image_contrast property
linktitle: image_contrast property
articleTitle: image_contrast property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_contrast property. Gets or sets the contrast for the generated images."
type: docs
weight: 50
url: /tr/python-net/aspose.words.saving/imagesaveoptions/image_contrast/
---

## ImageSaveOptions.image_contrast property

Gets or sets the contrast for the generated images.


```python
@property
def image_contrast(self) -> float:
    ...

@image_contrast.setter
def image_contrast(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.




### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Belgeyi bir görüntü olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
# Kaydetme işlemi görüntüyü render ederken resmi düzenleyin.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Bu özellikleri görüntünün parlaklığını ve kontrastını değiştirmek için ayarlayabiliriz.
# İkisi de 0-1 ölçeğinde ve varsayılan olarak 0.5'tedir.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Bu özelliklerle yatay ve dikey çözünürlüğü ayarlayabiliriz.
# Bu, görüntünün boyutlarını etkileyecek.
# Bu özelliklerin varsayılan değeri 96.0'dır, 96dpi çözünürlük için.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Bu özelliği kullanarak görüntüyü ölçeklendirebiliriz. Varsayılan değer %100 ölçekleme için 1.0'dır.
# Çözünürlüğü değiştirmenin neden olacağı görüntü boyutlarındaki değişiklikleri iptal etmek için bu özelliği kullanabiliriz.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

