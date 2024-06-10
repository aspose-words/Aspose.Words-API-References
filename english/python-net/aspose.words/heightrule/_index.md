---
title: HeightRule enumeration
linktitle: HeightRule enumeration
articleTitle: HeightRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.HeightRule enumeration. Specifies the rule for determining the height of an object."
type: docs
weight: 470
url: /python-net/aspose.words/heightrule/
---

## HeightRule enumeration

Specifies the rule for determining the height of an object.


### Members

| Name | Description |
| --- | --- |
| AT_LEAST | The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object. |
| EXACTLY | The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated. |
| AUTO | The height will grow automatically to accommodate all text inside an object. |

### Examples

Shows how to format rows with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# Start a second row, and then configure its height. The builder will apply these settings to
# its current row, as well as any new rows it creates afterwards.
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# The first row was unaffected by the padding reconfiguration and still holds the default values.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words](../)

