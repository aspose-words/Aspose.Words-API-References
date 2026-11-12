---
title: ImageData.gray_scale property
linktitle: gray_scale property
articleTitle: gray_scale property
second_title: Aspose.Words for Python
description: "ImageData.gray_scale property. Determines whether a picture will display in grayscale mode."
type: docs
weight: 100
url: /ru/python-net/aspose.words.drawing/imagedata/gray_scale/
---

## ImageData.gray_scale property

Determines whether a picture will display in grayscale mode.


```python
@property
def gray_scale(self) -> bool:
    ...

@gray_scale.setter
def gray_scale(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Импортируйте фигуру из исходного документа и добавьте её в первый абзац.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# Импортированная фигура содержит изображение. Мы можем получить доступ к свойствам изображения и его необработанным данным через объект ImageData.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Если у изображения нет границ, его объект ImageData определит цвет границы как пустой.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Это изображение не ссылается на другую форму или файл изображения в локальной файловой системе.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Свойства "Brightness" и "Contrast" определяют яркость и контраст изображения
# по шкале от 0 до 1, со значением по умолчанию 0.5.
image_data.brightness = 0.8
image_data.contrast = 1
# Указанные выше значения яркости и контраста создали изображение с большим количеством белого.
# Мы можем выбрать цвет с помощью свойства ChromaKey для замены его прозрачностью, например белый.
image_data.chroma_key = aspose.pydrawing.Color.white
# Снова импортируйте исходную форму и установите изображение в монохромный режим.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Снова импортируйте исходную форму, чтобы создать третье изображение, и установите его в режим BiLevel.
# BiLevel устанавливает каждый пиксель либо в черный, либо в белый цвет, в зависимости от того, какой ближе к исходному цвету.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Обрезка определяется по шкале от 0 до 1. Обрезка стороны на 0.3
# будет обрезать 30% изображения с указанной стороны.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

