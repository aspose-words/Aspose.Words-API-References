---
title: FieldComments.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldComments.text property. Gets or sets the text of the comments."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldcomments/text/
---

## FieldComments.text property

Gets or sets the text of the comments.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the COMMENTS field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Установите значение встроенного свойства документа "Comments".
doc.built_in_document_properties.comments = 'My comment.'
# Создайте поле COMMENTS, чтобы отобразить значение этого встроенного свойства.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True).as_field_comments()
field.update()
self.assertEqual(' COMMENTS ', field.get_field_code())
self.assertEqual('My comment.', field.result)
# Если мы зададим свойству Text поля COMMENTS значение и обновим его, поле будет
# перезаписывать текущее значение встроенного свойства "Comments" значением его свойства Text,
# а затем отображать новое значение.
field.text = 'My overriding comment.'
field.update()
self.assertEqual(' COMMENTS  "My overriding comment."', field.get_field_code())
self.assertEqual('My overriding comment.', field.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.COMMENTS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldComments](../)

