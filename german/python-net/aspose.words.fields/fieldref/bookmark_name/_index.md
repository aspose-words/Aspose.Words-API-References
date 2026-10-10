---
title: FieldRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldRef.bookmark_name property. Gets or sets the referenced bookmark's name."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldref/bookmark_name/
---

## FieldRef.bookmark_name property

Gets or sets the referenced bookmark's name.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
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
# Wir werden ein benutzerdefiniertes Listenformat anwenden, bei dem die Anzahl der spitzen Klammern die aktuelle Liststufe anzeigt.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# Fügen Sie ein REF-Feld ein, das den Text innerhalb unseres Lesezeichens enthält, als Hyperlink fungiert und die Fußnoten des Lesezeichens dupliziert.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# Fügen Sie ein REF-Feld ein und zeigen Sie an, ob das referenzierte Lesezeichen darüber oder darunter liegt.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# Zeigen Sie die Listennummer des Lesezeichens an, wie sie im Dokument erscheint.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# Zeigen Sie die Listennummer des Lesezeichens an, jedoch ohne Nicht-Trennzeichen wie die spitzen Klammern.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# Eine Liststufe nach unten gehen.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# Zeigen Sie die Listennummer des Lesezeichens und die Nummern aller darüber liegenden Liststufen an.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Zeigen Sie die Liststufennummern zwischen diesem REF-Feld und dem referenzierten Lesezeichen an.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# Am Ende des Dokuments wird das Lesezeichen hier als Listeneintrag angezeigt.
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

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Benennen Sie den markierten Text mit einem SET‑Feld.
# Dieses Feld bezieht sich auf das "bookmark", nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
field_set = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SET, update_field=False).as_field_set()
field_set.bookmark_name = 'MyBookmark'
field_set.bookmark_text = 'Hello world!'
field_set.update()
self.assertEqual(' SET  MyBookmark "Hello world!"', field_set.get_field_code())
# Verweisen Sie im REF‑Feld per Name auf das Lesezeichen und zeigen Sie dessen Inhalt an.
field_ref = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
field_ref.bookmark_name = 'MyBookmark'
field_ref.update()
self.assertEqual(' REF  MyBookmark', field_ref.get_field_code())
self.assertEqual('Hello world!', field_ref.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.SET.REF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

