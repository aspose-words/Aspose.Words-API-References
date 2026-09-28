---
title: HeightRule enumeration
linktitle: HeightRule enumeration
articleTitle: HeightRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.HeightRule enumeration. Specifies the rule for determining the height of an object."
type: docs
weight: 510
url: /zh/python-net/aspose.words/heightrule/
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
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# 启动第二行，然后配置其高度。构建器将把这些设置应用于
# 它当前的行以及之后创建的任何新行。
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# 第一行未受填充重新配置的影响，仍保持默认值。
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words](../)

