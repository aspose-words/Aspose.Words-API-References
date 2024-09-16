---
title: BuiltInDocumentProperties.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.title property. Gets or sets the title of the document."
type: docs
weight: 290
url: /python-net/aspose.words.properties/builtindocumentproperties/title/
---

## BuiltInDocumentProperties.title property

Gets or sets the title of the document.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# Below are four built-in document properties that have fields that can display their values in the document body.
# 1 -  "Author" property, which we can display using an AUTHOR field:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  "Title" property, which we can display using a TITLE field:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  "Subject" property, which we can display using a SUBJECT field:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  "Comments" property, which we can display using a COMMENTS field:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# The "Category" built-in property does not have a field that can display its value.
properties.category = 'My category'
# We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
# The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

