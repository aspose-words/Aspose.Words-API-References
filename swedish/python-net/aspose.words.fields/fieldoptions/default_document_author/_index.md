---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /sv/python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


```python
@property
def default_document_author(self) -> str:
    ...

@default_document_author.setter
def default_document_author(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# AUTHOR-fält hämtar sina resultat från den inbyggda dokumentegenskapen som heter "Author".
# Om vi skapar och sparar ett dokument i Microsoft Word,
# kommer det att ha vårt användarnamn i den egenskapen.
# Men om vi skapar ett dokument programmässigt med Aspose.Words,
# "Author"-egenskapen kommer som standard att vara en tom sträng.
self.assertEqual('', doc.built_in_document_properties.author)
# Ange ett reservförfattarnamn för AUTHOR-fält att använda
# om "Author"-egenskapen innehåller en tom sträng.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Uppdatera ett AUTHOR-fält som innehåller ett värde
# kommer att tillämpa det värdet på den inbyggda "Author"-egenskapen.
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Om du ändrar denna egenskap och sedan uppdaterar AUTHOR-fältet kommer detta värde att tillämpas på fältet.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Om vi uppdaterar ett AUTHOR-fält efter att ha ändrat dess "Name"-egenskap,
# kommer fältet att visa det nya namnet och tillämpa det nya namnet på den inbyggda egenskapen.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# AUTHOR-fält påverkar inte DefaultDocumentAuthor-egenskapen.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

