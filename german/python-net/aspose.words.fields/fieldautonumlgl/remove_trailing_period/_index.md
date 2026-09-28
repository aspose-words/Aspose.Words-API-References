---
title: FieldAutoNumLgl.remove_trailing_period property
linktitle: remove_trailing_period property
articleTitle: remove_trailing_period property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.remove_trailing_period property. Gets or sets whether to display the number without a trailing period."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldautonumlgl/remove_trailing_period/
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
# AUTONUMLGL-Felder zeigen eine Nummer an, die bei jedem AUTONUMLGL-Feld innerhalb seiner aktuellen Überschriftenebene erhöht wird.
# Diese Felder führen für jede Überschriftenebene einen separaten Zähler,
# und jedes Feld zeigt außerdem die AUTONUMLGL-Feldzähler für alle Überschriftenebenen unterhalb seiner eigenen an.
# Das Ändern der Zählung für jede Überschriftsebene setzt die Zählungen für alle darüber liegenden Ebenen auf 1 zurück.
# Dies ermöglicht es uns, unser Dokument in Form einer Gliederungsliste zu organisieren.
# Dies ist das erste AUTONUMLGL-Feld auf einer Überschriftsebene von 1, das im Dokument "1." anzeigt.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Dies ist das zweite AUTONUMLGL-Feld auf einer Überschriftsebene von 1, also wird es "2." anzeigen.
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Dies ist das erste AUTONUMLGL-Feld auf einer Überschriftsebene von 2,
# und die AUTONUMLGL-Zählung für die darunter liegende Überschriftsebene ist "2", also wird sie "2.1." anzeigen.
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Dies ist das erste AUTONUMLGL-Feld auf einer Überschriftsebene von 3.
# Es arbeitet auf dieselbe Weise wie das Feld darüber und wird "2.1.1." anzeigen.
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Dieses Feld befindet sich auf einer Überschriftsebene von 2, und seine jeweilige AUTONUMLGL-Zählung ist 2, also wird das Feld "2.2." anzeigen.
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Das Erhöhen der AUTONUMLGL-Zählung für eine darunter liegende Überschriftsebene
# hat die Zählung für diese Ebene zurückgesetzt, sodass dieses Feld "2.2.1." anzeigt.
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Das Trennzeichen, das im Feldresultat unmittelbar nach der Zahl erscheint,
    # ist standardmäßig ein Punkt. Wenn wir diese Eigenschaft null lassen,
    # wird unser letztes AUTONUMLGL-Feld im Dokument "2.2.1." anzeigen.
    self.assertIsNone(field.separator_character)
    # Das Festlegen eines benutzerdefinierten Trennzeichens und das Entfernen des abschließenden Punktes
    # wird das Erscheinungsbild dieses Feldes von "2.2.1." zu "2:2:1" ändern.
    # Wir werden dies auf alle Felder anwenden, die wir erstellt haben.
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
    # Dieser Text gehört zu dem auto num legal Feld darüber.
    # Es wird zusammengeklappt, wenn wir in Microsoft Word auf den Pfeil neben dem entsprechenden AUTONUMLGL-Feld klicken.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

