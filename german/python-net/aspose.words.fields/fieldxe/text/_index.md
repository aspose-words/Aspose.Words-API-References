---
title: FieldXE.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldXE.text property. Gets or sets the text of the entry."
type: docs
weight: 70
url: /de/python-net/aspose.words.fields/fieldxe/text/
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
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Feldes auf der linken Seite an
# und die Seite, die das XE-Feld enthält, auf der rechten Seite.
# Wenn die XE-Felder denselben Wert in ihrer "Text"-Eigenschaft haben,
# wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Konfigurieren Sie das INDEX-Feld so, dass nur XE-Felder angezeigt werden, die innerhalb der Grenzen
# eines Lesezeichens namens "MainBookmark" liegen und deren "EntryType"-Eigenschaften den Wert "A" haben.
# Für sowohl INDEX- als auch XE-Felder verwendet die "EntryType"-Eigenschaft nur das erste Zeichen ihres Zeichenkettenwerts.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# Auf einer neuen Seite beginnen Sie das Lesezeichen mit einem Namen, der dem Wert entspricht
# der "BookmarkName"-Eigenschaft des INDEX-Feldes.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# Das INDEX-Feld wird diesen Eintrag übernehmen, weil er sich innerhalb des Lesezeichens befindet,
# und sein Eintragstyp ebenfalls dem Eintragstyp des INDEX-Feldes entspricht.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Fügen Sie ein XE-Feld ein, das nicht im INDEX erscheint, weil die Eintragstypen nicht übereinstimmen.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Beenden Sie das Lesezeichen und fügen Sie anschließend ein XE-Feld ein.
# Es ist vom selben Typ wie das INDEX-Feld, erscheint jedoch nicht
# da es außerhalb der Grenzen des Lesezeichens liegt.
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
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Wenn die XE-Felder denselben Wert in ihrer "Text"-Eigenschaft haben,
# wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Wenn dieser Eigenschaftswert auf \"A\" gesetzt wird, werden alle Einträge nach ihrem ersten Buchstaben gruppiert,
# und dieser Buchstabe wird in Großbuchstaben über jeder Gruppe platziert.
index.heading = 'A'
# Stellen Sie die vom INDEX‑Feld erstellte Tabelle so ein, dass sie über 2 Spalten reicht.
index.number_of_columns = '2'
# Lassen Sie alle Einträge mit Anfangsbuchstaben außerhalb des Zeichenbereichs \"a-c\" weg.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Die nächsten beiden XE‑Felder erscheinen unter der Überschrift \"A\",
# wobei ihre jeweiligen Textformatierungen ebenfalls auf die Seitenzahlen angewendet werden.
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
# Die beiden nächsten XE‑Felder stehen unter den Überschriften \"B\" bzw. \"C\" im Inhaltsverzeichnis der INDEX‑Felder.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# INDEX‑Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag zusammen mit den anderen beiden unter \"A\" erscheint.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Dieser Eintrag wird nicht angezeigt, weil er mit dem Buchstaben \"D\" beginnt,
# was außerhalb des Zeichenbereichs \"a-c\" liegt, den die LetterRange‑Eigenschaft des INDEX‑Feldes definiert.
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

