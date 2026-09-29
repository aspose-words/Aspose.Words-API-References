---
title: FieldAdvance.down_offset property
linktitle: down_offset property
articleTitle: down_offset property
second_title: Aspose.Words for Python
description: "FieldAdvance.down_offset property. Gets or sets the number of points by which the text that follows the field should be moved down."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldadvance/down_offset/
---

## FieldAdvance.down_offset property

Gets or sets the number of points by which the text that follows the field should be moved down.


```python
@property
def down_offset(self) -> str:
    ...

@down_offset.setter
def down_offset(self, value: str):
    ...

```

### Examples

Shows how to insert an ADVANCE field, and edit its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('This text is in its normal place.')
# Ниже представлены два способа использования поля ADVANCE для корректировки позиции следующего за ним текста.
# Эффекты поля ADVANCE продолжают применяться до конца абзаца,
# или другое поле ADVANCE обновит значения смещения/координат.
# 1 -  Укажите направленное смещение:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.right_offset = '5'
field.up_offset = '5'
self.assertEqual(' ADVANCE  \\r 5 \\u 5', field.get_field_code())
builder.write('This text will be moved up and to the right.')
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.down_offset = '5'
field.left_offset = '100'
self.assertEqual(' ADVANCE  \\d 5 \\l 100', field.get_field_code())
builder.writeln('This text is moved down and to the left, overlapping the previous text.')
# 2 -  Переместите текст в позицию, указанную координатами:
field = builder.insert_field(aw.fields.FieldType.FIELD_ADVANCE, True).as_field_advance()
field.horizontal_position = '-100'
field.vertical_position = '200'
self.assertEqual(' ADVANCE  \\x -100 \\y 200', field.get_field_code())
builder.write('This text is in a custom position.')
doc.save(ARTIFACTS_DIR + 'Field.field_advance.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAdvance](../)

