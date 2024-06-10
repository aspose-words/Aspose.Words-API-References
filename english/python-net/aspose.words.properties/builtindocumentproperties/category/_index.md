---
title: BuiltInDocumentProperties.category property
linktitle: category property
articleTitle: category property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.category property. Gets or sets the category of the document."
type: docs
weight: 40
url: /python-net/aspose.words.properties/builtindocumentproperties/category/
---

## BuiltInDocumentProperties.category property

Gets or sets the category of the document.


```python
@property
def category(self) -> str:
    ...

@category.setter
def category(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
properties = doc.built_in_document_properties
# Below are four built-in document properties that have fields that can display their values in the document body.
# 1 -  "author" property, which we can display using an AUTHOR field:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(aw.fields.FieldType.FIELD_AUTHOR, True)
# 2 -  "title" property, which we can display using a TITLE field:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(aw.fields.FieldType.FIELD_TITLE, True)
# 3 -  "subject" property, which we can display using a SUBJECT field:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(aw.fields.FieldType.FIELD_SUBJECT, True)
# 4 -  "comments" property, which we can display using a COMMENTS field:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(aw.fields.FieldType.FIELD_COMMENTS, True)
builder.write('"')
# The "category" built-in property does not have a field that can display its value.
properties.category = 'My category'
# We can set multiple keywords for a document by separating the string value of the "keywords" property with semicolons.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
# The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc.save(ARTIFACTS_DIR + 'DocumentProperties.description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

