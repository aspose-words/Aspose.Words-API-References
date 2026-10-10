---
title: FieldIndex.use_yomi property
linktitle: use_yomi property
articleTitle: use_yomi property
second_title: Aspose.Words for Python
description: "FieldIndex.use_yomi property. Gets or sets whether to enable the use of yomi text for index entries."
type: docs
weight: 170
url: /de/python-net/aspose.words.fields/fieldindex/use_yomi/
---

## FieldIndex.use_yomi property

Gets or sets whether to enable the use of yomi text for index entries.


```python
@property
def use_yomi(self) -> bool:
    ...

@use_yomi.setter
def use_yomi(self, value: bool):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Der INDEX-Eintrag sammelt alle XE-Felder mit passenden Werten in der Eigenschaft "Text"
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Die INDEX-Tabelle sortiert ihre Einträge automatisch alphabetisch nach den Werten ihrer Text‑Eigenschaften.
# Stellen Sie die INDEX-Tabelle so ein, dass Einträge phonetisch mit Hiragana sortiert werden.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# Fügen Sie 4 XE-Felder ein, die als Einträge im Inhaltsverzeichnis des INDEX-Feldes erscheinen würden.
# Die "Text"-Eigenschaft kann die Schreibweise eines Wortes in Kanji enthalten, deren Aussprache mehrdeutig sein kann,
# während die "Yomi"-Version des Wortes exakt wiedergibt, wie es in Hiragana ausgesprochen wird.
# Wenn wir unser INDEX-Feld so einstellen, dass es Yomi verwendet, sortiert es diese Einträge
# nach dem Wert ihrer Yomi-Eigenschaften, statt ihrer Text-Werte.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

