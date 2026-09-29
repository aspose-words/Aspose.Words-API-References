---
title: FieldXE.yomi property
linktitle: yomi property
articleTitle: yomi property
second_title: Aspose.Words for Python
description: "FieldXE.yomi property. Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry"
type: docs
weight: 80
url: /it/python-net/aspose.words.fields/fieldxe/yomi/
---

## FieldXE.yomi property

Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry


```python
@property
def yomi(self) -> str:
    ...

@yomi.setter
def yomi(self, value: str):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# L'entrata INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà \"Text\"
# in una sola voce anziché creare una voce per ogni campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# La tabella INDEX ordina automaticamente le sue voci in base ai valori delle loro proprietà Text in ordine alfabetico.
# Imposta la tabella INDEX per ordinare le voci foneticamente usando Hiragana invece.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# Inserisci 4 campi XE, che appariranno come voci nell'indice della tabella dei contenuti del campo INDEX.
# La proprietà "Text" può contenere l'ortografia di una parola in Kanji, la cui pronuncia può essere ambigua,
# mentre la versione "Yomi" della parola indicherà esattamente come è pronunciata usando Hiragana.
# Se impostiamo il nostro campo INDEX per usare Yomi, ordinerà queste voci
# in base al valore delle loro proprietà Yomi, invece che ai valori della proprietà Text.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

