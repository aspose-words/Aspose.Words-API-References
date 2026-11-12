---
title: BuiltInDocumentProperties.subject property
linktitle: subject property
articleTitle: subject property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.subject property. Gets or sets the subject of the document."
type: docs
weight: 290
url: /tr/python-net/aspose.words.properties/builtindocumentproperties/subject/
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
# Aşağıda, değerlerini belge gövdesinde görüntüleyebilen alanlara sahip dört yerleşik belge özelliği bulunmaktadır.
# 1 - "Author" özelliği, bunu bir AUTHOR alanı kullanarak görüntüleyebiliriz:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 - "Title" özelliği, bunu bir TITLE alanı kullanarak görüntüleyebiliriz:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 - "Subject" özelliği, bunu bir SUBJECT alanı kullanarak görüntüleyebiliriz:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 - "Comments" özelliği, bunu bir COMMENTS alanı kullanarak görüntüleyebiliriz:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# "Category" yerleşik özelliğinin değerini görüntüleyebilecek bir alanı yoktur.
properties.category = 'My category'
# "Keywords" özelliğinin dize değerini noktalı virgüllerle ayırarak bir belgeye birden fazla anahtar kelime atayabiliriz.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Windows Explorer'da bu belgeye sağ tıklayabilir ve bu özellikleri "Properties" -> "Details" altında bulabiliriz.
# "Author" yerleşik özelliği "Origin" grubunda, diğerleri ise "Description" grubunda yer alır.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

