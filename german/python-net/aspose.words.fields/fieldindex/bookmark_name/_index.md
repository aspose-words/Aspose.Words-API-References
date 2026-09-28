---
title: FieldIndex.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldIndex.bookmark_name property. Gets or sets the name of the bookmark that marks the portion of the document used to build the index."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldindex/bookmark_name/
---

## FieldIndex.bookmark_name property

Gets or sets the name of the bookmark that marks the portion of the document used to build the index.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
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

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

