---
title: FieldIndex.page_range_separator property
linktitle: page_range_separator property
articleTitle: page_range_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_range_separator property. Gets or sets the character sequence that is used to separate the start and end of a page range."
type: docs
weight: 130
url: /it/python-net/aspose.words.fields/fieldindex/page_range_separator/
---

## FieldIndex.page_range_separator property

Gets or sets the character sequence that is used to separate the start and end of a page range.


```python
@property
def page_range_separator(self) -> str:
    ...

@page_range_separator.setter
def page_range_separator(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# L'entrata INDEX raccoglierà tutti i campi XE con valori corrispondenti nella proprietà \"Text\"
# in una sola voce anziché creare una voce per ogni campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Per le voci INDEX che mostrano intervalli di pagine, possiamo specificare una stringa separatore
# che apparirà tra il numero della prima pagina e il numero dell'ultima.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Se un campo XE nomina un segnalibro usando la proprietà PageRangeBookmarkName,
# la sua voce INDEX mostrerà l'intervallo di pagine che il segnalibro copre
# invece del numero della pagina che contiene il campo XE.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Inserisci un segnalibro che inizia a pagina 3 e termina a pagina 5.
# La voce INDEX per il campo XE che fa riferimento a questo segnalibro mostrerà questo intervallo di pagine.
# Nella nostra tabella, la voce INDEX mostrerà "My entry, on page(s) 3 to 5".
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MyBookmark')
builder.write('Start of MyBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('End of MyBookmark')
builder.end_bookmark('MyBookmark')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageRangeBookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

