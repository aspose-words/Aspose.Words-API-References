---
title: FieldAuthor.author_name property
linktitle: author_name property
articleTitle: author_name property
second_title: Aspose.Words for Python
description: "FieldAuthor.author_name property. Gets or sets the document author's name."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldauthor/author_name/
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
# Les champs AUTHOR tirent leurs résultats de la propriété de document intégrée appelée "Author".
# Si nous créons et enregistrons un document dans Microsoft Word,
# il contiendra notre nom d'utilisateur dans cette propriété.
# Cependant, si nous créons un document de manière programmatique en utilisant Aspose.Words,
# la propriété "Author", par défaut, sera une chaîne vide.
self.assertEqual('', doc.built_in_document_properties.author)
# Définissez un nom d'auteur de secours que les champs AUTHOR utiliseront
# si la propriété "Author" contient une chaîne vide.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Mettre à jour un champ AUTHOR qui contient une valeur
# appliquera cette valeur à la propriété intégrée "Author".
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Modifier cette propriété, puis mettre à jour le champ AUTHOR appliquera cette valeur au champ.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Si nous mettons à jour un champ AUTHOR après avoir modifié sa propriété "Name",
# alors le champ affichera le nouveau nom et appliquera ce nouveau nom à la propriété intégrée.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# Les champs AUTHOR n'affectent pas la propriété DefaultDocumentAuthor.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAuthor](../)

