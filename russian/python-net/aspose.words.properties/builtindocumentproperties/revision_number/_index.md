---
title: BuiltInDocumentProperties.revision_number property
linktitle: revision_number property
articleTitle: revision_number property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.revision_number property. Gets or sets the document revision number."
type: docs
weight: 250
url: /ru/python-net/aspose.words.properties/builtindocumentproperties/revision_number/
---

## BuiltInDocumentProperties.revision_number property

Gets or sets the document revision number.


```python
@property
def revision_number(self) -> int:
    ...

@revision_number.setter
def revision_number(self, value: int):
    ...

```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to work with REVNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Current revision #')
# Вставьте поле REVNUM, которое отображает свойство текущего номера ревизии документа.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REVISION_NUM, update_field=True).as_field_rev_num()
self.assertEqual(' REVNUM ', field.get_field_code())
self.assertEqual('1', field.result)
self.assertEqual(1, doc.built_in_document_properties.revision_number)
# Это свойство считает, сколько раз документ был сохранён в Microsoft Word,
# и не связано с отслеживаемыми изменениями. Мы можем найти его, щёлкнув правой кнопкой мыши по документу в Проводнике Windows
# через Свойства -> Подробности. Мы можем обновить это свойство вручную.
doc.built_in_document_properties.revision_number += 1
field.update()
self.assertEqual('2', field.result)
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

