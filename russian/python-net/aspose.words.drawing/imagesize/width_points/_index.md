---
title: ImageSize.width_points property
linktitle: width_points property
articleTitle: width_points property
second_title: Aspose.Words for Python
description: "ImageSize.width_points property. Gets the width of the image in points"
type: docs
weight: 70
url: /ru/python-net/aspose.words.drawing/imagesize/width_points/
---

## ImageSize.width_points property

Gets the width of the image in points. 1 point is 1/72 inch.


```python
@property
def width_points(self) -> float:
    ...

```

### Examples

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
* class [ImageSize](../)

