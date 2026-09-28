---
title: FieldXE.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldXE.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /de/python-net/aspose.words.fields/fieldxe/page_range_bookmark_name/
---

## FieldXE.page_range_bookmark_name property

Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.


```python
@property
def page_range_bookmark_name(self) -> str:
    ...

@page_range_bookmark_name.setter
def page_range_bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Der INDEX-Eintrag sammelt alle XE-Felder mit passenden Werten in der Eigenschaft "Text"
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Für INDEX-Einträge, die Seitenbereiche anzeigen, können wir eine Trennzeichenzeichenfolge angeben
# die zwischen der Nummer der ersten Seite und der Nummer der letzten erscheint.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Wenn ein XE-Feld ein Lesezeichen mit der PageRangeBookmarkName-Eigenschaft benennt,
# wird sein INDEX-Eintrag den Seitenbereich anzeigen, den das Lesezeichen umfasst
# statt der Seitenzahl, die das XE-Feld enthält.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Fügen Sie ein Lesezeichen ein, das auf Seite 3 beginnt und auf Seite 5 endet.
# Der INDEX-Eintrag für das XE-Feld, das auf dieses Lesezeichen verweist, zeigt diesen Seitenbereich an.
# In unserer Tabelle wird der INDEX-Eintrag "My entry, on page(s) 3 to 5" anzeigen.
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
* class [FieldXE](../)

