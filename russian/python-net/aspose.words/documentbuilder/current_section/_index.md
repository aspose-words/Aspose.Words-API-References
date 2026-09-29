---
title: DocumentBuilder.current_section property
linktitle: current_section property
articleTitle: current_section property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_section property. Gets the section that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 60
url: /ru/python-net/aspose.words/documentbuilder/current_section/
---

## DocumentBuilder.current_section property

Gets the section that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_section(self) -> aspose.words.Section:
    ...

```

### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Настройте свойство формы "RelativeHorizontalPosition" так, чтобы оно учитывало значение свойства "Left"
# как горизонтальное расстояние формы в пунктах от левой стороны страницы.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Установите горизонтальное расстояние формы от левой стороны страницы в 100.
shape.left = 100
# Используйте свойство "RelativeVerticalPosition" аналогичным образом, чтобы разместить форму на 80 пунктов ниже верхней части страницы.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Установите высоту формы, при этом ширина будет автоматически масштабироваться для сохранения пропорций.
shape.height = 125
self.assertEqual(125, shape.width)
# Свойства "Bottom" и "Right" содержат нижний и правый края изображения.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

