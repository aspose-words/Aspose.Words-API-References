---
title: ImageSaveOptions.image_brightness property
linktitle: image_brightness property
articleTitle: image_brightness property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_brightness property. Gets or sets the brightness for the generated images."
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/imagesaveoptions/image_brightness/
---

## ImageSaveOptions.image_brightness property

Gets or sets the brightness for the generated images.


```python
@property
def image_brightness(self) -> float:
    ...

@image_brightness.setter
def image_brightness(self, value: float):
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
# При сохранении документа в виде изображения мы можем передать объект SaveOptions к
# отредактируйте изображение, пока операция сохранения его рендерит.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Мы можем настроить эти свойства, чтобы изменить яркость и контраст изображения.
# Оба находятся в диапазоне от 0 до 1 и по умолчанию равны 0,5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Мы можем настроить горизонтальное и вертикальное разрешение с помощью этих свойств.
# Это повлияет на размеры изображения.
# Значение по умолчанию для этих свойств равно 96,0 при разрешении 96dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0, что соответствует масштабированию 100%.
# Мы можем использовать это свойство, чтобы отменить любые изменения размеров изображения, которые могут возникнуть при изменении разрешения.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

