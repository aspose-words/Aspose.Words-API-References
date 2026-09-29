---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /it/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# L'entrata INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà \"Text\"
# in una sola voce anziché creare una voce per ogni campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# Campi XE che hanno una proprietà Text il cui valore diventa l'intestazione della voce INDEX.
# Se questo valore contiene due segmenti di stringa separati da due punti (la voce INDEX tratterà :) come delimitatore,
# il primo segmento è l'intestazione, e il secondo segmento diventerà il sottotitolo.
# Il campo INDEX raggruppa prima le voci alfabeticamente, poi, se ci sono più campi XE con lo stesso
# intestazioni, il campo INDEX le suddividerà ulteriormente in base ai valori di queste intestazioni.
# Possono esserci più livelli di suddivisione, a seconda di quante volte
# le proprietà Text dei campi XE vengono segmentate in questo modo.
# Per impostazione predefinita, un gruppo di voci del campo INDEX crea una nuova riga per ogni sottotitolo all'interno di questo gruppo.
# Possiamo impostare il flag RunSubentriesOnSameLine su true per mantenere il titolo,
# e ogni sottotitolo per il gruppo su un'unica riga, il che renderà il campo INDEX più compatto.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Inserisci due campi XE, ciascuno su una nuova pagina, e con lo stesso titolo denominato "Heading 1",
# che il campo INDEX utilizzerà per raggrupparli.
# Se RunSubentriesOnSameLine è false, la tabella INDEX creerà tre righe:
# una riga per il titolo di raggruppamento "Heading 1", e un'altra riga per ogni sottotitolo.
# Se RunSubentriesOnSameLine è true, la tabella INDEX creerà una riga unica
# che comprende il titolo e tutti i sottotitoli.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

