---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /it/python-net/aspose.words.fields/fieldoptions/default_document_author/
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
# I campi AUTHOR ottengono i risultati dalla proprietà incorporata del documento chiamata "Author".
# Se creiamo e salviamo un documento in Microsoft Word,
# avrà il nostro nome utente in quella proprietà.
# Tuttavia, se creiamo un documento programmaticamente usando Aspose.Words,
# la proprietà "Author", per impostazione predefinita, sarà una stringa vuota.
self.assertEqual('', doc.built_in_document_properties.author)
# Imposta un nome autore di riserva da utilizzare per i campi AUTHOR
# se la proprietà "Author" contiene una stringa vuota.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Aggiornare un campo AUTHOR che contiene un valore
# applicherà quel valore alla proprietà incorporata "Author".
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Modificando questa proprietà, quindi aggiornando il campo AUTHOR, si applicherà questo valore al campo.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Se aggiorniamo un campo AUTHOR dopo aver modificato la sua proprietà "Name",
# allora il campo visualizzerà il nuovo nome e lo applicherà alla proprietà incorporata.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# I campi AUTHOR non influenzano la proprietà DefaultDocumentAuthor.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

