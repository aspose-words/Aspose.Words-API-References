---
title: FieldXE class
linktitle: FieldXE class
articleTitle: FieldXE class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldXE class. Implements the XE field"
type: docs
weight: 1150
url: /de/python-net/aspose.words.fields/fieldxe/
---

## FieldXE class

Implements the XE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Defines the text and page number for an index entry, which is used by an INDEX field.


**Inheritance:** [FieldXE](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldXE()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_type](./entry_type/) | Gets or sets an index entry type. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_bold](./is_bold/) | Gets or sets whether to apply bold formatting to the entry's page number. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_italic](./is_italic/) | Gets or sets whether to apply italic formatting to the entry's page number. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_replacement](./page_number_replacement/) | Gets or sets text used in place of a page number. |
| [page_range_bookmark_name](./page_range_bookmark_name/) | Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text](./text/) | Gets or sets the text of the entry. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [yomi](./yomi/) | Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

