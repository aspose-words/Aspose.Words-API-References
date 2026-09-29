---
title: FieldIndex.entry_type property
linktitle: entry_type property
articleTitle: entry_type property
second_title: Aspose.Words for Python
description: "FieldIndex.entry_type property. Gets or sets an index entry type used to build the index."
type: docs
weight: 40
url: /it/python-net/aspose.words.fields/fieldindex/entry_type/
---

## FieldIndex.entry_type property

Gets or sets an index entry type used to build the index.


```python
@property
def entry_type(self) -> str:
    ...

@entry_type.setter
def entry_type(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro
# e la pagina contenente il campo XE sul lato destro.
# Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
# il campo INDEX li raggrupperà in un'unica voce.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Configura il campo INDEX in modo che visualizzi solo i campi XE che si trovano entro i limiti
# di un segnalibro chiamato "MainBookmark", e le cui proprietà "EntryType" hanno valore "A".
# Per entrambi i campi INDEX e XE, la proprietà "EntryType" utilizza solo il primo carattere del valore stringa.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# Su una nuova pagina, avvia il segnalibro con un nome che corrisponde al valore
# della proprietà "BookmarkName" del campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# Il campo INDEX prenderà questa voce perché è all'interno del segnalibro,
# e il suo tipo di voce corrisponde anche al tipo di voce del campo INDEX.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Inserisci un campo XE che non apparirà nell'INDEX perché i tipi di voce non corrispondono.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Chiudi il segnalibro e inserisci un campo XE successivamente.
# È dello stesso tipo del campo INDEX, ma non apparirà
# poiché è al di fuori dei limiti del segnalibro.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

