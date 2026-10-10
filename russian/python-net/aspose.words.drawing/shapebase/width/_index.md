---
title: ShapeBase.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "ShapeBase.width property. Gets or sets the width of the containing block of the shape."
type: docs
weight: 610
url: /ru/python-net/aspose.words.drawing/shapebase/width/
---

## ShapeBase.width property

Gets or sets the width of the containing block of the shape.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




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

Shows how to resize a shape with an image.

```python
# Когда мы вставляем изображение с помощью метода "InsertImage", конструктор масштабирует фигуру, отображающую изображение, так чтобы,
# при просмотре документа с масштабом 100% в Microsoft Word, фигура отображает изображение в его реальном размере.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Изображение 400x400 создаст объект ImageData с размером изображения 300x300pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Если размеры фигуры совпадают с размерами данных изображения,
# то фигура отображает изображение в его оригинальном размере.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Уменьшите общий размер фигуры на 50%.
# Коэффициенты масштабирования применяются одновременно к ширине и высоте, чтобы сохранить пропорции фигуры.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# При изменении размера фигуры размер данных изображения остаётся прежним.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Мы можем использовать размеры данных изображения, чтобы применить масштабирование на основе размера изображения.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

