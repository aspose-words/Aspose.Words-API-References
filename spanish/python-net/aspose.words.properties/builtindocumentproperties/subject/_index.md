---
title: BuiltInDocumentProperties.subject property
linktitle: subject property
articleTitle: subject property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.subject property. Gets or sets the subject of the document."
type: docs
weight: 290
url: /es/python-net/aspose.words.properties/builtindocumentproperties/subject/
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
# A continuación se presentan cuatro propiedades de documento incorporadas que tienen campos que pueden mostrar sus valores en el cuerpo del documento.
# 1 -  propiedad "Author", que podemos mostrar usando un campo AUTHOR:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  propiedad "Title", que podemos mostrar usando un campo TITLE:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  propiedad "Subject", que podemos mostrar usando un campo SUBJECT:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  propiedad "Comments", que podemos mostrar usando un campo COMMENTS:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# La propiedad incorporada "Category" no tiene un campo que pueda mostrar su valor.
properties.category = 'My category'
# Podemos establecer múltiples palabras clave para un documento separando el valor de cadena de la propiedad "Keywords" con puntos y comas.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Podemos hacer clic derecho en este documento en el Explorador de Windows y encontrar estas propiedades en "Properties" -> "Details".
# La propiedad incorporada "Author" está en el grupo "Origin", y las demás están en el grupo "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

