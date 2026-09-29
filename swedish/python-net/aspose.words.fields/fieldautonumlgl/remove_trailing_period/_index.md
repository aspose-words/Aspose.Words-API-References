---
title: FieldAutoNumLgl.remove_trailing_period property
linktitle: remove_trailing_period property
articleTitle: remove_trailing_period property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.remove_trailing_period property. Gets or sets whether to display the number without a trailing period."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldautonumlgl/remove_trailing_period/
---

## FieldAutoNumLgl.remove_trailing_period property

Gets or sets whether to display the number without a trailing period.


```python
@property
def remove_trailing_period(self) -> bool:
    ...

@remove_trailing_period.setter
def remove_trailing_period(self, value: bool):
    ...

```

### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# AUTONUMLGL-fält visar ett nummer som ökas vid varje AUTONUMLGL-fält inom dess nuvarande rubriknivå.
# Dessa fält upprätthåller en separat räknare för varje rubriknivå,
# och varje fält visar också AUTONUMLGL-fältens räknare för alla rubriknivåer under sin egen.
# Att ändra räknaren för någon rubriknivå återställer räknarna för alla nivåer ovanför den nivån till 1.
# Detta gör att vi kan organisera vårt dokument i form av en dispositionslista.
# Detta är det första AUTONUMLGL-fältet på rubriknivå 1, som visar "1." i dokumentet.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Detta är det andra AUTONUMLGL-fältet på rubriknivå 1, så det kommer att visa "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Detta är det första AUTONUMLGL-fältet på rubriknivå 2,
# och AUTONUMLGL-räkningen för rubriknivån under den är "2", så den kommer att visa "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Detta är det första AUTONUMLGL-fältet på rubriknivå 3.
# Det fungerar på samma sätt som fältet ovan och kommer att visa "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Detta fält är på rubriknivå 2, och dess motsvarande AUTONUMLGL-räkning är 2, så fältet kommer att visa "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Att öka AUTONUMLGL-räkningen för en rubriknivå under denna
# har återställt räknaren för den här nivån så att detta fält kommer att visa "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Separatortecknet, som visas i fältresultatet omedelbart efter siffran,
    # är en punkt som standard. Om vi lämnar den här egenskapen null,
    # kommer vårt sista AUTONUMLGL-fält att visa "2.2.1." i dokumentet.
    self.assertIsNone(field.separator_character)
    # Att ange ett anpassat separatortecken och ta bort den avslutande punkten
    # kommer att ändra fältets utseende från "2.2.1." till "2:2:1".
    # Vi kommer att tillämpa detta på alla fält som vi har skapat.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # Denna text kommer att tillhöra auto num legal-fältet ovanför den.
    # Det kommer att kollapsa när vi klickar på pilen bredvid motsvarande AUTONUMLGL-fält i Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

