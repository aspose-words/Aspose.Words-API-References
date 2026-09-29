---
title: FieldRef.insert_paragraph_number_in_relative_context property
linktitle: insert_paragraph_number_in_relative_context property
articleTitle: insert_paragraph_number_in_relative_context property
second_title: Aspose.Words for Python
description: "FieldRef.insert_paragraph_number_in_relative_context property. Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context."
type: docs
weight: 70
url: /it/python-net/aspose.words.fields/fieldref/insert_paragraph_number_in_relative_context/
---

## FieldRef.insert_paragraph_number_in_relative_context property

Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context.


```python
@property
def insert_paragraph_number_in_relative_context(self) -> bool:
    ...

@insert_paragraph_number_in_relative_context.setter
def insert_paragraph_number_in_relative_context(self, value: bool):
    ...

```

### Examples

Shows how to insert REF fields to reference bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #1')
builder.write('Text that will appear in REF field')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #2')
builder.end_bookmark('MyBookmark')
builder.move_to_document_start()
# Applicheremo un formato di elenco personalizzato, dove il numero di parentesi angolari indica il livello di elenco in cui ci troviamo.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# Inserisci un campo REF che conterrà il testo all'interno del nostro segnalibro, agirà come collegamento ipertestuale e clonerà le note a piè di pagina del segnalibro.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# Inserisci un campo REF e visualizza se il segnalibro di riferimento è sopra o sotto di esso.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# Visualizza il numero di elenco del segnalibro così come appare nel documento.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# Visualizza il numero di elenco del segnalibro, ma omettendo i caratteri non delimitatori, come le parentesi angolari.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# Scendi di un livello di elenco.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# Visualizza il numero di elenco del segnalibro e i numeri di tutti i livelli di elenco superiori.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Visualizza i numeri dei livelli di elenco tra questo campo REF e il segnalibro a cui fa riferimento.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# Alla fine del documento, il segnalibro apparirà qui come elemento di elenco.
builder.writeln('List level above bookmark')
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>>> \x02'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.REF.docx')
```

Shows how to insert REF fields to reference bookmarks (InsertFieldRef).

```python
@staticmethod
def _insert_field_ref(builder, bookmark_name, text_before, text_after):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
    field.bookmark_name = bookmark_name
    builder.write(text_after)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

