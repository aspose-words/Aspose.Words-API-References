---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/fieldxe/page_number_replacement/
---

## FieldXE.page_number_replacement property

Gets or sets text used in place of a page number.


```python
@property
def page_number_replacement(self) -> str:
    ...

@page_number_replacement.setter
def page_number_replacement(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# L'entrata INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà \"Text\"
# in una sola voce anziché creare una voce per ogni campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Possiamo configurare un campo XE affinché la sua voce INDEX visualizzi una stringa invece di un numero di pagina.
# Prima, per le voci che sostituiscono un numero di pagina con una stringa,
# specifica un separatore personalizzato tra il valore della proprietà Text del campo XE e la stringa.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Inserisci un campo XE, che crea una voce INDEX regolare che visualizza il numero di pagina di questo campo,
# e non richiama il valore CrossReferenceSeparator.
# La voce per questo campo XE visualizzerà \"Apple, 2\".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Inserisci un altro campo XE a pagina 3 e imposta un valore per la proprietà PageNumberReplacement.
# Questo valore apparirà al posto del numero della pagina su cui si trova questo campo,
# e il valore CrossReferenceSeparator del campo INDEX apparirà davanti ad esso.
# La voce per questo campo XE visualizzerà \"Banana, see: Tropical fruit\".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

