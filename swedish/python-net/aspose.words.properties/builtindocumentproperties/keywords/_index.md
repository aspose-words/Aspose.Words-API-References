---
title: BuiltInDocumentProperties.keywords property
linktitle: keywords property
articleTitle: keywords property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.keywords property. Gets or sets the document keywords."
type: docs
weight: 150
url: /sv/python-net/aspose.words.properties/builtindocumentproperties/keywords/
---

## BuiltInDocumentProperties.keywords property

Gets or sets the document keywords.


```python
@property
def keywords(self) -> str:
    ...

@keywords.setter
def keywords(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# Nedan finns fyra inbyggda dokumentegenskaper som har fält som kan visa sina värden i dokumentkroppen.
# 1 -  "Author"-egenskapen, som vi kan visa med ett AUTHOR-fält:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  "Title"-egenskapen, som vi kan visa med ett TITLE-fält:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  "Subject"-egenskapen, som vi kan visa med ett SUBJECT-fält:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  "Comments"-egenskapen, som vi kan visa med ett COMMENTS-fält:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# "Category"-egenskapen har inget fält som kan visa dess värde.
properties.category = 'My category'
# Vi kan ange flera nyckelord för ett dokument genom att separera strängvärdet för "Keywords"-egenskapen med semikolon.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Vi kan högerklicka på detta dokument i Windows Explorer och hitta dessa egenskaper i "Properties" -> "Details".
# "Author"-egenskapen finns i gruppen "Origin", och de andra finns i gruppen "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

