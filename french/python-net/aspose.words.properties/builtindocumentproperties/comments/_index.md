---
title: BuiltInDocumentProperties.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.comments property. Gets or sets the document comments."
type: docs
weight: 70
url: /fr/python-net/aspose.words.properties/builtindocumentproperties/comments/
---

## BuiltInDocumentProperties.comments property

Gets or sets the document comments.


```python
@property
def comments(self) -> str:
    ...

@comments.setter
def comments(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# Voici quatre propriétés de document intégrées qui possèdent des champs pouvant afficher leurs valeurs dans le corps du document.
# 1 -  propriété "Author", que nous pouvons afficher à l'aide d'un champ AUTHOR :
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  propriété "Title", que nous pouvons afficher à l'aide d'un champ TITLE :
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  propriété "Subject", que nous pouvons afficher à l'aide d'un champ SUBJECT :
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  propriété "Comments", que nous pouvons afficher à l'aide d'un champ COMMENTS :
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# La propriété intégrée "Category" n'a pas de champ pouvant afficher sa valeur.
properties.category = 'My category'
# Nous pouvons définir plusieurs mots-clés pour un document en séparant la valeur chaîne de la propriété "Keywords" par des points-virgules.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# Nous pouvons faire un clic droit sur ce document dans l'Explorateur Windows et trouver ces propriétés dans "Properties" -> "Details".
# La propriété intégrée "Author" se trouve dans le groupe "Origin", et les autres sont dans le groupe "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

