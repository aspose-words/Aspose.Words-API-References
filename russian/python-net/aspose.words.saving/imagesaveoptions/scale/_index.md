---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /ru/python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Remarks

The default value is 1.0. The value must be greater than 0.


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

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Создайте объект "ImageSaveOptions", который будет передан методу "Save" рендерера узлов для изменения
# того, как он рендерит узел OfficeMath в изображение.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Установите свойство "Scale" в значение 5, чтобы отрисовать объект в пять раз больше его исходного размера.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

