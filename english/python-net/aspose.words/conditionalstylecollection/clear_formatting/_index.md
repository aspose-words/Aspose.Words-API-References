---
title: ConditionalStyleCollection.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "ConditionalStyleCollection.clear_formatting method. Clears all conditional styles of the table style."
type: docs
weight: 150
url: /python-net/aspose.words/conditionalstylecollection/clear_formatting/
---

## clear_formatting() {#default}

Clears all conditional styles of the table style.


```python
def clear_formatting(self):
    ...
```

### Examples

Shows how to reset conditional table styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("First row")
builder.end_row()
builder.insert_cell()
builder.write("Last row")
builder.end_table()

table_style = doc.styles.add(aw.StyleType.TABLE, "MyTableStyle1").as_table_style()
table.style = table_style

# Set the table style to color the borders of the first row of the table in red.
table_style.conditional_styles.first_row.borders.color = drawing.Color.red

# Set the table style to color the borders of the last row of the table in blue.
table_style.conditional_styles.last_row.borders.color = drawing.Color.blue

# Below are two ways of using the "clear_formatting" method to clear the conditional styles.
# 1 -  Clear the conditional styles for a specific part of a table:
table_style.conditional_styles[0].clear_formatting()

self.assertEqual(drawing.Color.empty(), table_style.conditional_styles.first_row.borders.color)

# 2 -  Clear the conditional styles for the entire table:
table_style.conditional_styles.clear_formatting()

self.assertTrue(all(s.borders.color == drawing.Color.empty()
                    for s in table_style.conditional_styles))
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyleCollection](../)

