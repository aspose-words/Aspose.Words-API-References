---
title: FieldIndex.letter_range property
linktitle: letter_range property
articleTitle: letter_range property
second_title: Aspose.Words for Python
description: "FieldIndex.letter_range property. Gets or sets a range of letters to which limit the index."
type: docs
weight: 90
url: /de/python-net/aspose.words.fields/fieldindex/letter_range/
---

## FieldIndex.letter_range property

Gets or sets a range of letters to which limit the index.


```python
@property
def letter_range(self) -> str:
    ...

@letter_range.setter
def letter_range(self, value: str):
    ...

```

### Examples

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
* class [FieldIndex](../)

