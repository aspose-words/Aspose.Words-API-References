---
title: FieldNoteRef.insert_reference_mark property
linktitle: insert_reference_mark property
articleTitle: insert_reference_mark property
second_title: Aspose.Words for Python
description: "FieldNoteRef.insert_reference_mark property. Inserts the reference mark with the same character formatting as the Footnote Reference or Endnote Reference style."
type: docs
weight: 40
url: /it/python-net/aspose.words.fields/fieldnoteref/insert_reference_mark/
---

## FieldNoteRef.insert_reference_mark property

Inserts the reference mark with the same character formatting as the Footnote Reference
or Endnote Reference style.


```python
@property
def insert_reference_mark(self) -> bool:
    ...

@insert_reference_mark.setter
def insert_reference_mark(self, value: bool):
    ...

```

### Examples

Shows to insert NOTEREF fields, and modify their appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un segnalibro con una nota a pié di pagina che il campo NOTEREF farà riferimento.
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# Questo campo NOTEREF visualizzerà il numero della nota a pié di pagina all'interno del segnalibro di riferimento.
# Impostare la proprietà InsertHyperlink ci consente di passare al segnalibro premendo Ctrl + clic sul campo in Microsoft Word.
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# Quando si utilizza il flag \p, dopo il numero della nota a pié di pagina, il campo visualizza anche la posizione del segnalibro rispetto al campo.
# Bookmark1 è sopra questo campo e contiene il numero della nota a pié di pagina 1, quindi il risultato sarà "1 sopra" all'aggiornamento.
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# Bookmark2 è sotto questo campo e contiene il numero della nota a pié di pagina 2, quindi il campo visualizzerà "2 sotto".
# Il flag \f fa apparire il numero 2 nello stesso formato dell'etichetta del numero della nota a pié di pagina nel testo reale.
self.assertEqual(' NOTEREF  MyBookmark2 \\h \\p \\f', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, True, True, 'Bookmark2, with footnote number ').get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark2', 'Contents of MyBookmark2', 'Footnote from MyBookmark2')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.NOTEREF.docx')
```

Shows to insert NOTEREF fields, and modify their appearance (InsertFieldNoteRef).

```python
@staticmethod
def _insert_field_note_ref(builder, bookmark_name, insert_hyperlink, insert_relative_position, insert_reference_mark, text_before):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NOTE_REF, update_field=True).as_field_note_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    field.insert_reference_mark = insert_reference_mark
    builder.writeln()
    return field

@staticmethod
def _insert_bookmark_with_footnote(builder, bookmark_name, bookmark_text, footnote_text):
    builder.start_bookmark(bookmark_name)
    builder.write(bookmark_text)
    builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=footnote_text)
    builder.end_bookmark(bookmark_name)
    builder.writeln()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldNoteRef](../)

