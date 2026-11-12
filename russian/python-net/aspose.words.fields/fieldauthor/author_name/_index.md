---
title: FieldAuthor.author_name property
linktitle: author_name property
articleTitle: author_name property
second_title: Aspose.Words for Python
description: "FieldAuthor.author_name property. Gets or sets the document author's name."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldauthor/author_name/
---

## FieldAuthor.author_name property

Gets or sets the document author's name.


```python
@property
def author_name(self) -> str:
    ...

@author_name.setter
def author_name(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поля AUTHOR получают свои результаты из встроенного свойства документа под названием "Author".
# Если мы создаём и сохраняем документ в Microsoft Word,
# в этом свойстве будет указано наше имя пользователя.
# Однако, если мы создаём документ программно с помощью Aspose.Words,
# свойство "Author" по умолчанию будет пустой строкой.
self.assertEqual('', doc.built_in_document_properties.author)
# Установите резервное имя автора, которое будут использовать поля AUTHOR
# если свойство "Author" содержит пустую строку.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Обновление поля AUTHOR, содержащего значение
# применит это значение к встроенному свойству "Author".
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Изменив это свойство, а затем обновив поле AUTHOR, вы примените это значение к полю.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Если мы обновим поле AUTHOR после изменения его свойства "Name",
# то поле отобразит новое имя и применит новое имя к встроенному свойству.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# Поля AUTHOR не влияют на свойство DefaultDocumentAuthor.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAuthor](../)

