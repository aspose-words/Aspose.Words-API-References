---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поле BIDIOUTLINE нумерует абзацы так же, как поля AUTONUM/LISTNUM,
# но оно видно только при включённом языке редактирования справа налево, таком как иврит или арабский.
# Следующее поле отобразит ".1", RTL‑эквивалент номера списка "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Добавьте ещё два поля BIDIOUTLINE, которые отобразят ".2" и ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Установите горизонтальное выравнивание текста для каждого абзаца в документе в RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Если мы включим язык редактирования справа налево в Microsoft Word, наши поля будут отображать числа.
# В противном случае они отобразят "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Откройте документ, созданный в Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Если открыть документ Word и нажать Alt+F9, мы увидим поле SHAPE и поле EMBED.
# Поле SHAPE является якорем/холстом для объекта AutoShape с включённым стилем обтекания «В строке с текстом».
# Поле EMBED выполняет ту же функцию, но для встроенного объекта,
# например, таблицы из внешнего документа Excel.
# Однако эти поля не появятся в коллекции Fields документа.
self.assertEqual(0, doc.range.fields.count)
# Эти поля поддерживаются только старыми версиями Microsoft Word.
# Процесс загрузки документа преобразует эти поля в объекты Shape,
# к которым мы можем получить доступ в коллекции узлов документа.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Первый узел Shape соответствует полю SHAPE во входном документе,
# который является встроенным холстом для AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Второй узел Shape — это сам AutoShape.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Третий Shape — это то, что было полем EMBED, содержащим внешнюю таблицу.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

