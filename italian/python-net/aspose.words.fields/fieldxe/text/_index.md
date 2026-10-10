---
title: FieldXE.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldXE.text property. Gets or sets the text of the entry."
type: docs
weight: 70
url: /it/python-net/aspose.words.fields/fieldxe/text/
---

## FieldXE.text property

Gets or sets the text of the entry.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
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

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
# il campo INDEX li raggrupperà in un'unica voce.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Impostare il valore di questa proprietà su "A" raggrupperà tutte le voci per la loro prima lettera,
# e posizionerà quella lettera in maiuscolo sopra ogni gruppo.
index.heading = 'A'
# Imposta la tabella creata dal campo INDEX in modo che si estenda su 2 colonne.
index.number_of_columns = '2'
# Imposta che tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "a-c" vengano omesse.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# I prossimi due campi XE appariranno sotto l'intestazione "A",
# con i rispettivi stili di testo applicati anche ai numeri di pagina.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Entrambi i prossimi due campi XE saranno sotto le intestazioni "B" e "C" nel sommario dei campi INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# I campi INDEX ordinano tutte le voci alfabeticamente, quindi questa voce apparirà sotto "A" insieme alle altre due.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Questa voce non apparirà perché inizia con la lettera "D",
# che è al di fuori dell'intervallo di caratteri "a-c" definito dalla proprietà LetterRange del campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

