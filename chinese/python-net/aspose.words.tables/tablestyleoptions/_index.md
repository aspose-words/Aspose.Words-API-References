---
title: TableStyleOptions enumeration
linktitle: TableStyleOptions enumeration
articleTitle: TableStyleOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.TableStyleOptions enumeration. Specifies how table style is applied to a table."
type: docs
weight: 150
url: /zh/python-net/aspose.words.tables/tablestyleoptions/
---

## TableStyleOptions enumeration

Specifies how table style is applied to a table.


### Members

| Name | Description |
| --- | --- |
| NONE | No table style formatting is applied. |
| FIRST_ROW | Apply first row conditional formatting. |
| LAST_ROW | Apply last row conditional formatting. |
| FIRST_COLUMN | Apply 1 first column conditional formatting. |
| LAST_COLUMN | Apply last column conditional formatting. |
| ROW_BANDS | Apply row banding conditional formatting. |
| COLUMN_BANDS | Apply column banding conditional formatting. |
| DEFAULT2003 | Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF. |
| DEFAULT | This is Microsoft Word defaults. |

### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# 在设置任何表格格式之前，必须先插入至少一行。
builder.insert_cell()
# 根据样式标识符设置使用的表格样式。
# 请注意，保存为 .doc 格式时并非所有表格样式都可用。
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1
# 根据谓词将样式部分应用于表格的特性，然后构建表格。
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

* module [aspose.words.tables](../)
* property [Table.style_options](../table/style_options/)

