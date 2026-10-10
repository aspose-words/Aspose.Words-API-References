---
title: FieldIndex.has_page_number_separator property
linktitle: has_page_number_separator property
articleTitle: has_page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.has_page_number_separator property. Gets a value indicating whether a page number separator is overridden through the field's code."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/fieldindex/has_page_number_separator/
---

## FieldIndex.has_page_number_separator property

Gets a value indicating whether a page number separator is overridden through the field's code.


```python
@property
def has_page_number_separator(self) -> bool:
    ...

```

### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Text"
# in una sola voce anziché creare una voce per ogni campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Se il nostro campo INDEX ha una voce per un gruppo di campi XE,
# questa voce mostrerà il numero di ogni pagina che contiene un campo XE appartenente a questo gruppo.
# Possiamo impostare separatori personalizzati per personalizzare l'aspetto di questi numeri di pagina.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# Dopo aver inserito questi campi XE, il campo INDEX visualizzerà "Prima voce, su pagina(e) 2 & 3 & 4".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
self.assertEqual(' XE  "First entry"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageNumberList.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

