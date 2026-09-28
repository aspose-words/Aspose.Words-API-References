---
title: FieldIndex.page_number_separator property
linktitle: page_number_separator property
articleTitle: page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_number_separator property. Gets or sets the character sequence that is used to separate an index entry and its page number."
type: docs
weight: 120
url: /de/python-net/aspose.words.fields/fieldindex/page_number_separator/
---

## FieldIndex.page_number_separator property

Gets or sets the character sequence that is used to separate an index entry and its page number.


```python
@property
def page_number_separator(self) -> str:
    ...

@page_number_separator.setter
def page_number_separator(self, value: str):
    ...

```

### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Der INDEX-Eintrag wird XE-Felder mit übereinstimmenden Werten in der "Text"-Eigenschaft gruppieren
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Wenn unser INDEX-Feld einen Eintrag für eine Gruppe von XE-Feldern hat,
# wird dieser Eintrag die Nummer jeder Seite anzeigen, die ein XE-Feld enthält, das zu dieser Gruppe gehört.
# Wir können benutzerdefinierte Trennzeichen festlegen, um das Aussehen dieser Seitenzahlen anzupassen.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# Nachdem wir diese XE-Felder eingefügt haben, zeigt das INDEX-Feld "Erster Eintrag, auf Seite(n) 2 & 3 & 4" an.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
self.assertEqual(' XE  "First entry"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageNumberList.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

