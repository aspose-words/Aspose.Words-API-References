---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /sv/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
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
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# INDEX‑posten kommer att samla alla XE‑fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# XE-fält som har en Text-egenskap vars värde blir rubriken för INDEX-posten.
# Om detta värde innehåller två strängsegment separerade med ett kolon (INDEX-posten kommer att behandla :) som avgränsare,
# så är det första segmentet rubrik, och det andra segmentet blir underrubrik.
# INDEX-fältet grupperar först poster alfabetiskt, sedan, om det finns flera XE-fält med samma
# rubriker, kommer INDEX-fältet att ytterligare undergruppera dem efter värdena för dessa rubriker.
# Det kan finnas flera undergrupperingsnivåer, beroende på hur många gånger
# Text-egenskaperna för XE-fält segmenteras på detta sätt.
# Som standard kommer en INDEX-fältpostgrupp att skapa en ny rad för varje underrubrik inom denna grupp.
# Vi kan sätta flaggan RunSubentriesOnSameLine till true för att behålla rubriken,
# och varje underrubrik för gruppen på en rad istället, vilket gör INDEX-fältet mer kompakt.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Infoga två XE-fält, vardera på en ny sida, och med samma rubrik benämnd "Heading 1",
# som INDEX-fältet kommer att använda för att gruppera dem.
# Om RunSubentriesOnSameLine är false, kommer INDEX-tabellen att skapa tre rader:
# en rad för grupprubriken "Heading 1", och ytterligare en rad för varje underrubrik.
# Om RunSubentriesOnSameLine är true, kommer INDEX-tabellen att skapa en enradig
# post som omfattar rubriken och varje underrubrik.
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

