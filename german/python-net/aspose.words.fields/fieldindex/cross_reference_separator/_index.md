---
title: FieldIndex.cross_reference_separator property
linktitle: cross_reference_separator property
articleTitle: cross_reference_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.cross_reference_separator property. Gets or sets the character sequence that is used to separate cross references and other entries."
type: docs
weight: 30
url: /de/python-net/aspose.words.fields/fieldindex/cross_reference_separator/
---

## FieldIndex.cross_reference_separator property

Gets or sets the character sequence that is used to separate cross references and other entries.


```python
@property
def cross_reference_separator(self) -> str:
    ...

@cross_reference_separator.setter
def cross_reference_separator(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Der INDEX-Eintrag sammelt alle XE-Felder mit passenden Werten in der Eigenschaft "Text"
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Wir können ein XE-Feld so konfigurieren, dass sein INDEX-Eintrag einen String anstelle einer Seitenzahl anzeigt.
# Zuerst für Einträge, die eine Seitenzahl durch einen String ersetzen,
# geben Sie einen benutzerdefinierten Trennzeichen zwischen dem Text‑Eigenschaftswert des XE-Feldes und dem String an.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Fügen Sie ein XE-Feld ein, das einen regulären INDEX-Eintrag erzeugt, der die Seitenzahl dieses Feldes anzeigt,
# und den Wert CrossReferenceSeparator nicht verwendet.
# Der Eintrag für dieses XE-Feld zeigt "Apple, 2" an.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Fügen Sie auf Seite 3 ein weiteres XE-Feld ein und setzen Sie einen Wert für die Eigenschaft PageNumberReplacement.
# Dieser Wert wird anstelle der Seitenzahl angezeigt, auf der sich dieses Feld befindet,
# und der Wert CrossReferenceSeparator des INDEX-Feldes erscheint davor.
# Der Eintrag für dieses XE-Feld zeigt "Banana, see: Tropical fruit" an.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

