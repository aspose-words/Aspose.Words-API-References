---
title: Table.auto_fit method
linktitle: auto_fit method
articleTitle: auto_fit method
second_title: Aspose.Words for Python
description: "Table.auto_fit method. Resizes the table and cells according to the specified auto fit behavior."
type: docs
weight: 360
url: /python-net/aspose.words.tables/table/auto_fit/
---

## auto_fit(behavior) {#autofitbehavior}

Resizes the table and cells according to the specified auto fit behavior.


```python
def auto_fit(self, behavior: aspose.words.tables.AutoFitBehavior):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| behavior | [AutoFitBehavior](../../autofitbehavior/) | Specifies how to auto fit the table. |

### Remarks

This method mimics the commands available in the Auto Fit menu for a table in Microsoft Word.
The commands available are "Auto Fit to Contents", "Auto Fit to Window" and "Fixed Column Width". In Microsoft Word
these commands set relevant table properties and then update the table layout and Aspose.Words does the same for you.




### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()

# We must insert at least one row before setting any table formatting.
builder.insert_cell()

# Set the table style used based on the style identifier.
# Note that not all table styles are available when saving to .doc format.
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1

# Partially apply the style to features of the table based on predicates, then build the table.
table.style_options = aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS | aw.tables.TableStyleOptions.FIRST_ROW
table.auto_fit(aw.tables.AutoFitBehavior.AUTO_FIT_TO_CONTENTS)

builder.writeln("Item")
builder.cell_format.right_padding = 40
builder.insert_cell()
builder.writeln("Quantity (kg)")
builder.end_row()

builder.insert_cell()
builder.writeln("Apples")
builder.insert_cell()
builder.writeln("20")
builder.end_row()

builder.insert_cell()
builder.writeln("Bananas")
builder.insert_cell()
builder.writeln("40")
builder.end_row()

builder.insert_cell()
builder.writeln("Carrots")
builder.insert_cell()
builder.writeln("50")
builder.end_row()

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table_with_style.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

