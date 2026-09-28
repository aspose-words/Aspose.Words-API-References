---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /de/python-net/aspose.words.fields/fieldoptions/default_document_author/
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
# AUTHOR-Felder beziehen ihre Ergebnisse aus der integrierten Dokumenteigenschaft "Author".
# Wenn wir ein Dokument in Microsoft Word erstellen und speichern,
# enthält es unseren Benutzernamen in dieser Eigenschaft.
# Wenn wir jedoch ein Dokument programmgesteuert mit Aspose.Words erstellen,
# ist die Eigenschaft "Author" standardmäßig eine leere Zeichenkette.
self.assertEqual('', doc.built_in_document_properties.author)
# Legen Sie einen Ersatzautornamen fest, den AUTHOR-Felder verwenden sollen
# wenn die Eigenschaft "Author" eine leere Zeichenkette enthält.
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# Aktualisieren eines AUTHOR-Feldes, das einen Wert enthält
# wird diesen Wert auf die integrierte Eigenschaft "Author" anwenden.
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# Wenn diese Eigenschaft geändert und anschließend das AUTHOR-Feld aktualisiert wird, wird dieser Wert auf das Feld angewendet.
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# Wenn wir ein AUTHOR-Feld nach dem Ändern seiner "Name"-Eigenschaft aktualisieren,
# zeigt das Feld dann den neuen Namen an und überträgt den neuen Namen auf die integrierte Eigenschaft.
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# AUTHOR-Felder beeinflussen die Eigenschaft DefaultDocumentAuthor nicht.
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

