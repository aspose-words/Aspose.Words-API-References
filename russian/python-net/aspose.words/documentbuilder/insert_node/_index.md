---
title: DocumentBuilder.insert_node method
linktitle: insert_node method
articleTitle: insert_node method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_node method. Inserts a node before the cursor."
type: docs
weight: 410
url: /ru/python-net/aspose.words/documentbuilder/insert_node/
---

## insert_node(node) {#node}

Inserts a node before the cursor.


```python
def insert_node(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) |  |

### Examples

Shows how to insert a linked image into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
image_file_name = IMAGE_DIR + 'Windows MetaFile.wmf'
# Ниже представлены два способа применения изображения к фигуре, чтобы она могла его отобразить.
# 1 -  Установить фигуру, содержащую изображение.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.set_image(file_name=image_file_name)
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx')
# Каждое изображение, которое мы сохраняем в фигуре, увеличивает размер нашего документа.
self.assertTrue(70000 < system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Embedded.docx').length())
doc.first_section.body.first_paragraph.remove_all_children()
# 2 -  Установить фигуру, ссылающуюся на файл изображения в локальной файловой системе.
shape = aw.drawing.Shape(builder.document, aw.drawing.ShapeType.IMAGE)
shape.wrap_type = aw.drawing.WrapType.INLINE
shape.image_data.source_full_name = image_file_name
builder.insert_node(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx')
# Ссылка на изображения сэкономит место и приведёт к меньшему размеру документа.
# Однако документ может корректно отображать изображение только пока
# файл изображения находится в месте, на которое указывает свойство "SourceFullName" формы.
self.assertTrue(10000 > system_helper.io.FileInfo(ARTIFACTS_DIR + 'Image.CreateLinkedImage.Linked.docx').length())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

