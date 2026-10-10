---
title: FieldToa.sequence_name property
linktitle: sequence_name property
articleTitle: sequence_name property
second_title: Aspose.Words for Python
description: "FieldToa.sequence_name property. Gets or sets the name of a sequence whose number is included with the page number."
type: docs
weight: 80
url: /de/python-net/aspose.words.fields/fieldtoa/sequence_name/
---

## FieldToa.sequence_name property

Gets or sets the name of a sequence whose number is included with the page number.


```python
@property
def sequence_name(self) -> str:
    ...

@sequence_name.setter
def sequence_name(self, value: str):
    ...

```

### Examples

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein TOA‑Feld ein, das für jedes TA‑Feld im Dokument einen Eintrag erstellt,
# wobei für jeden Eintrag lange Zitate und Seitenzahlen angezeigt werden.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Legen Sie die Eintragskategorie für unsere Tabelle fest. Dieses TOA wird nun nur TA‑Felder enthalten
# die einen passenden Wert in ihrer Eigenschaft EntryCategory haben.
field_toa.entry_category = '1'
# Außerdem ist die Kategorie "Cases" im Table of Authorities an Index 1,
# die als Titel unserer Tabelle angezeigt wird, wenn wir diese Variable auf true setzen.
field_toa.use_heading = True
# Wir können TA‑Felder weiter filtern, indem wir ein Lesezeichen benennen, das innerhalb der TOA‑Grenzen liegen muss.
field_toa.bookmark_name = 'MyBookmark'
# Standardmäßig erscheint ein punktierter, seitenweiter Tabulator zwischen dem Zitat des TA‑Feldes
# und seiner Seitenzahl. Wir können ihn durch beliebigen Text ersetzen, den wir in dieser Eigenschaft angeben.
# Das Einfügen eines Tab‑Zeichens bewahrt den ursprünglichen Tabulator.
field_toa.entry_separator = ' \t p.'
# Wenn wir mehrere TA‑Einträge haben, die dasselbe lange Zitat teilen,
# werden alle zugehörigen Seitenzahlen in einer Zeile angezeigt.
# Wir können diese Eigenschaft verwenden, um eine Zeichenkette anzugeben, die ihre Seitenzahlen trennt.
field_toa.page_number_list_separator = ' & p. '
# Wir können dies auf true setzen, damit unsere Tabelle das Wort "passim" anzeigt.
# wenn es fünf oder mehr Seitenzahlen in einer Zeile gibt.
field_toa.use_passim = True
# Ein TA-Feld kann sich auf einen Seitenbereich beziehen.
# Wir können hier eine Zeichenkette angeben, die zwischen den Start- und Endseitenzahlen für solche Bereiche erscheint.
field_toa.page_range_separator = ' to '
# Das Format der TA-Felder wird in unsere Tabelle übernommen.
# Wir können dies deaktivieren, indem wir das RemoveEntryFormatting-Flag setzen.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Dieses TA-Feld wird nicht als Eintrag im TOA erscheinen, da es außerhalb ist
# der Lesezeichen-Grenzen, die die BookmarkName-Eigenschaft des TOA angibt.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Dieses TA-Feld befindet sich innerhalb des Lesezeichens,
# aber die Eintragskategorie stimmt nicht mit der der Tabelle überein, sodass das TA-Feld es nicht einschließt.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Dieser Eintrag wird in der Tabelle erscheinen.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Eine TOA-Tabelle zeigt keine Kurzzitate an,
# aber wir können sie als Abkürzung verwenden, um auf umfangreiche Quellennamen zu verweisen, die von mehreren TA-Feldern referenziert werden.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Wir können die Seitenzahl formatieren, um sie fett/kursiv zu machen, indem wir die folgenden Eigenschaften verwenden.
# Wir werden diese Effekte weiterhin sehen, wenn wir unsere Tabelle so einstellen, dass sie Formatierungen ignoriert.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Wir können TA-Felder konfigurieren, damit ihre TOA-Einträge sich auf einen Seitenbereich beziehen, den ein Lesezeichen umfasst.
# Beachten Sie, dass sich dieser Eintrag auf dieselbe Quelle bezieht wie der oben genannte, um eine Zeile in unserer Tabelle zu teilen.
# Diese Zeile wird die Seitenzahl des obigen Eintrags und den Seitenbereich dieses Eintrags enthalten,
# mit den Seitenlisten- und Seitenbereichstrennzeichen der Tabelle zwischen den Seitenzahlen.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Wenn wir die "Passim"-Funktion unserer Tabelle aktiviert haben, führt das Vorhandensein von 5 oder mehr TA-Einträgen mit derselben Quelle dazu.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToa](../)

