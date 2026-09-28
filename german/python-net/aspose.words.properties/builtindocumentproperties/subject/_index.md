---
title: BuiltInDocumentProperties.subject property
linktitle: subject property
articleTitle: subject property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.subject property. Gets or sets the subject of the document."
type: docs
weight: 290
url: /de/python-net/aspose.words.properties/builtindocumentproperties/subject/
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
# Nachfolgend sind vier integrierte Dokumenteigenschaften aufgeführt, die Felder besitzen, die ihre Werte im Dokumentkörper anzeigen können.
# 1 -  "Author"-Eigenschaft, die wir mit einem AUTHOR-Feld anzeigen können:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  "Title"-Eigenschaft, die wir mit einem TITLE-Feld anzeigen können:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  "Subject"-Eigenschaft, die wir mit einem SUBJECT-Feld anzeigen können:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  "Comments"-Eigenschaft, die wir mit einem COMMENTS-Feld anzeigen können:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# Die integrierte Eigenschaft "Category" hat kein Feld, das ihren Wert anzeigen kann.
properties.category = 'My category'
# Wir können mehrere Schlüsselwörter für ein Dokument festlegen, indem wir den Zeichenfolgenwert der "Keywords"-Eigenschaft mit Semikolons trennen.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Wir können dieses Dokument im Windows Explorer mit der rechten Maustaste anklicken und diese Eigenschaften unter "Properties" -> "Details" finden.
# Die integrierte Eigenschaft "Author" befindet sich in der Gruppe "Origin", und die anderen befinden sich in der Gruppe "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

