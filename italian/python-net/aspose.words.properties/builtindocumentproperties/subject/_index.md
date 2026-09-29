---
title: BuiltInDocumentProperties.subject property
linktitle: subject property
articleTitle: subject property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.subject property. Gets or sets the subject of the document."
type: docs
weight: 290
url: /it/python-net/aspose.words.properties/builtindocumentproperties/subject/
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
# Di seguito sono elencate quattro proprietà di documento integrate che hanno campi in grado di visualizzare i loro valori nel corpo del documento.
# 1 -  proprietà "Author", che possiamo visualizzare usando un campo AUTHOR:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  proprietà "Title", che possiamo visualizzare usando un campo TITLE:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  proprietà "Subject", che possiamo visualizzare usando un campo SUBJECT:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  proprietà "Comments", che possiamo visualizzare usando un campo COMMENTS:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# La proprietà integrata "Category" non ha un campo che possa visualizzare il suo valore.
properties.category = 'My category'
# Possiamo impostare più parole chiave per un documento separando il valore stringa della proprietà "Keywords" con punti e virgola.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Possiamo fare clic con il tasto destro su questo documento in Esplora file di Windows e trovare queste proprietà in "Properties" -> "Details".
# La proprietà integrata "Author" si trova nel gruppo "Origin", e le altre sono nel gruppo "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

