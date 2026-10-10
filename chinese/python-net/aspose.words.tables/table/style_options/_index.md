---
title: Table.style_options property
linktitle: style_options property
articleTitle: style_options property
second_title: Aspose.Words for Python
description: "Table.style_options property. Gets or sets bit flags that specify how a table style is applied to this table."
type: docs
weight: 300
url: /zh/python-net/aspose.words.tables/table/style_options/
---

## Table.style_options property

Gets or sets bit flags that specify how a table style is applied to this table.


```python
@property
def style_options(self) -> aspose.words.tables.TableStyleOptions:
    ...

@style_options.setter
def style_options(self, value: aspose.words.tables.TableStyleOptions):
    ...

```

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

* module [aspose.words.tables](../../)
* class [Table](../)

