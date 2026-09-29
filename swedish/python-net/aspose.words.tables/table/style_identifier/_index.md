---
title: Table.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "Table.style_identifier property. Gets or sets the locale independent style identifier of the table style applied to this table."
type: docs
weight: 280
url: /sv/python-net/aspose.words.tables/table/style_identifier/
---

## Table.style_identifier property

Gets or sets the locale independent style identifier of the table style applied to this table.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# Vi måste infoga minst en rad innan vi ställer in någon tabellformatering.
builder.insert_cell()
# Ange den tabellstil som ska användas baserat på stilidentifieraren.
# Observera att inte alla tabellstilar är tillgängliga när du sparar i .doc-format.
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1
# Tillämpa stilen delvis på tabellens funktioner baserat på predikat, och bygg sedan tabellen.
table.style_options = aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS | aw.tables.TableStyleOptions.FIRST_ROW
table.auto_fit(aw.tables.AutoFitBehavior.AUTO_FIT_TO_CONTENTS)
builder.writeln('Item')
builder.cell_format.right_padding = 40
builder.insert_cell()
builder.writeln('Quantity (kg)')
builder.end_row()
builder.insert_cell()
builder.writeln('Apples')
builder.insert_cell()
builder.writeln('20')
builder.end_row()
builder.insert_cell()
builder.writeln('Bananas')
builder.insert_cell()
builder.writeln('40')
builder.end_row()
builder.insert_cell()
builder.writeln('Carrots')
builder.insert_cell()
builder.writeln('50')
builder.end_row()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTableWithStyle.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

