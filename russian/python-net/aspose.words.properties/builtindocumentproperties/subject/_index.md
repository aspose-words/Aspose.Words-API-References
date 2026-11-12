---
title: BuiltInDocumentProperties.subject property
linktitle: subject property
articleTitle: subject property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.subject property. Gets or sets the subject of the document."
type: docs
weight: 290
url: /ru/python-net/aspose.words.properties/builtindocumentproperties/subject/
---

## BuiltInDocumentProperties.subject property

Gets or sets the subject of the document.


```python
@property
def subject(self) -> str:
    ...

@subject.setter
def subject(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# Ниже перечислены четыре встроенных свойства документа, для которых существуют поля, способные отображать их значения в теле документа.
# 1 -  свойство "Author", которое мы можем отобразить с помощью поля AUTHOR:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  свойство "Title", которое мы можем отобразить с помощью поля TITLE:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  свойство "Subject", которое мы можем отобразить с помощью поля SUBJECT:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  свойство "Comments", которое мы можем отобразить с помощью поля COMMENTS:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# Встроенное свойство "Category" не имеет поля, способного отобразить его значение.
properties.category = 'My category'
# Мы можем задать несколько ключевых слов для документа, разделив строковое значение свойства "Keywords" точками с запятой.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Мы можем щёлкнуть правой кнопкой мыши по этому документу в Проводнике Windows и найти эти свойства в разделе "Properties" -> "Details".
# Встроенное свойство "Author" находится в группе "Origin", а остальные — в группе "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

