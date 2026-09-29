---
title: FieldToa.page_number_list_separator property
linktitle: page_number_list_separator property
articleTitle: page_number_list_separator property
second_title: Aspose.Words for Python
description: "FieldToa.page_number_list_separator property. Gets or sets the character sequence that is used to separate two page numbers in a page number list."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/fieldtoa/page_number_list_separator/
---

## FieldToa.page_number_list_separator property

Gets or sets the character sequence that is used to separate two page numbers in a page number list.


```python
@property
def page_number_list_separator(self) -> str:
    ...

@page_number_list_separator.setter
def page_number_list_separator(self, value: str):
    ...

```

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci un campo TOA, che creerà una voce per ogni campo TA nel documento,
# visualizzando citazioni lunghe e numeri di pagina per ogni voce.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Imposta la categoria della voce per la nostra tabella. Questo TOA includerà ora solo i campi TA
# che hanno un valore corrispondente nella loro proprietà EntryCategory.
field_toa.entry_category = '1'
# Inoltre, la categoria Table of Authorities all'indice 1 è "Cases",
# che apparirà come titolo della nostra tabella se impostiamo questa variabile su true.
field_toa.use_heading = True
# Possiamo filtrare ulteriormente i campi TA assegnando un segnalibro entro i limiti del TOA.
field_toa.bookmark_name = 'MyBookmark'
# Per impostazione predefinita, una tabulazione a linea puntata su tutta la pagina appare tra la citazione del campo TA
# e il suo numero di pagina. Possiamo sostituirla con qualsiasi testo inserito in questa proprietà.
# Inserire un carattere di tabulazione manterrà la tabulazione originale.
field_toa.entry_separator = ' \t p.'
# Se abbiamo più voci TA che condividono la stessa citazione lunga,
# tutti i loro numeri di pagina corrispondenti appariranno su una sola riga.
# Possiamo usare questa proprietà per specificare una stringa che separerà i loro numeri di pagina.
field_toa.page_number_list_separator = ' & p. '
# Possiamo impostare questo su true per far sì che la nostra tabella mostri la parola "passim"
# se ci sono cinque o più numeri di pagina in una riga.
field_toa.use_passim = True
# Un campo TA può riferirsi a un intervallo di pagine.
# Possiamo specificare qui una stringa da far apparire tra i numeri di pagina iniziale e finale per tali intervalli.
field_toa.page_range_separator = ' to '
# Il formato dei campi TA verrà trasferito nella nostra tabella.
# Possiamo disabilitare questo impostando il flag RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Questo campo TA non apparirà come voce nel TOA poiché è al di fuori
# dei limiti del segnalibro specificati dalla proprietà BookmarkName del TOA.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Questo campo TA è all'interno del segnalibro,
# ma la categoria della voce non corrisponde a quella della tabella, quindi il campo TA non la includerà.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Questa voce apparirà nella tabella.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Una tabella TOA non visualizza citazioni brevi,
# ma possiamo usarle come abbreviazione per riferirci a nomi di fonti voluminosi che più campi TA citano.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Possiamo formattare il numero di pagina per renderlo grassetto/corsivo usando le seguenti proprietà.
# Vedremo comunque questi effetti se impostiamo la nostra tabella per ignorare la formattazione.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Possiamo configurare i campi TA affinché le loro voci TOA si riferiscano a un intervallo di pagine coperto da un segnalibro.
# Nota che questa voce si riferisce alla stessa fonte di quella sopra per condividere una riga nella nostra tabella.
# Questa riga avrà il numero di pagina della voce sopra e l'intervallo di pagine di questa voce,
# con l'elenco delle pagine della tabella e i separatori di intervallo di numeri di pagina tra i numeri di pagina.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Se abbiamo abilitato la funzione "Passim" della nostra tabella, avere 5 o più voci TA con la stessa fonte la attiverà.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToa](../)

