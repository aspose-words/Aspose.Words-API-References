---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /de/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Der INDEX-Eintrag sammelt alle XE-Felder mit passenden Werten in der Eigenschaft "Text"
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# XE-Felder, die eine Text‑Eigenschaft besitzen, deren Wert zur Überschrift des INDEX‑Eintrags wird.
# Wenn dieser Wert zwei Zeichenketten‑Segmente enthält, die durch einen Doppelpunkt getrennt sind (der INDEX‑Eintrag behandelt :) als Trennzeichen,
# ist das erste Segment die Überschrift und das zweite Segment wird zur Unterüberschrift.
# Das INDEX‑Feld gruppiert zuerst Einträge alphabetisch und dann, wenn es mehrere XE‑Felder mit demselben
# Überschriften gibt, wird das INDEX‑Feld sie weiter nach den Werten dieser Überschriften unterteilen.
# Es können mehrere Untergruppierungsebenen existieren, abhängig davon, wie oft
# die Text‑Eigenschaften von XE-Feldern auf diese Weise segmentiert werden.
# Standardmäßig erstellt eine INDEX-Feldeintragsgruppe für jede Unterüberschrift innerhalb dieser Gruppe eine neue Zeile.
# Wir können das Flag RunSubentriesOnSameLine auf true setzen, um die Überschrift beizubehalten,
# und jede Unterüberschrift der Gruppe stattdessen in einer Zeile zu halten, was das INDEX-Feld kompakter macht.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Fügen Sie zwei XE-Felder ein, jeweils auf einer neuen Seite, und mit derselben Überschrift namens "Heading 1",
# die das INDEX-Feld zur Gruppierung verwendet.
# Wenn RunSubentriesOnSameLine false ist, erstellt die INDEX-Tabelle drei Zeilen:
# eine Zeile für die Gruppierungsüberschrift "Heading 1" und jeweils eine weitere Zeile für jede Unterüberschrift.
# Wenn RunSubentriesOnSameLine true ist, erstellt die INDEX-Tabelle eine einzeilige
# Eintrag, der die Überschrift und jede Unterüberschrift umfasst.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

