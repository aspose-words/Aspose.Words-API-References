---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
# Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
# und die Seitenzahl, auf der das Feld erscheint.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfiguriere dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert "MySequence" hat.
field_toc.table_of_figures_label = 'MySequence'
# Konfiguriere dieses TOC-Feld so, dass es nur SEQ-Felder übernimmt, die innerhalb der Grenzen eines Lesezeichens liegen
# mit dem Namen "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Füge ein SEQ-Feld ein, das einen Sequenzbezeichner hat, der dem TOC's
# TableOfFiguresLabel-Eigenschaft. Dieses Feld wird keinen Eintrag im TOC erzeugen, da es außerhalb ist
# der vom Lesezeichen "BookmarkName" festgelegten Grenzen.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Die Sequenz dieses SEQ-Feldes stimmt mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein und liegt innerhalb der Lesezeichen-Grenzen.
# Der Absatz, der dieses Feld enthält, wird im TOC als Eintrag angezeigt.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Die Sequenz dieses SEQ-Feldes stimmt nicht mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein,
# liegt jedoch innerhalb der Lesezeichen-Grenzen. Sein Absatz wird im TOC nicht als Eintrag angezeigt.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Die Sequenz dieses SEQ-Feldes stimmt mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein und liegt innerhalb der Lesezeichen-Grenzen.
# Dieses Feld verweist außerdem auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens erscheint im TOC-Eintrag für dieses SEQ-Feld.
# Das SEQ-Feld selbst wird den Inhalt dieses Lesezeichens nicht anzeigen.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Erstelle ein Lesezeichen mit Inhalt, das im TOC-Eintrag erscheint, weil das obige SEQ-Feld darauf verweist.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

