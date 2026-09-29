---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ogni campo AUTONUM visualizza il valore corrente di un conteggio progressivo dei campi AUTONUM,
# consentendoci di numerare automaticamente gli elementi come in un elenco numerato.
# Questo campo visualizzerà un numero "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Il carattere separatore, che appare nel risultato del campo immediatamente dopo il numero, è un punto per impostazione predefinita.
# Se lasciamo questa proprietà null, il nostro secondo campo AUTONUM visualizzerà "2." nel documento.
self.assertIsNone(field.separator_character)
# Possiamo impostare questa proprietà per utilizzare il primo carattere della sua stringa come nuovo carattere separatore.
# In questo caso, il nostro campo AUTONUM visualizzerà ora "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

