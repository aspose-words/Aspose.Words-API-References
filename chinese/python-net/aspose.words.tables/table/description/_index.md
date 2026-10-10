---
title: Table.description property
linktitle: description property
articleTitle: description property
second_title: Aspose.Words for Python
description: "Table.description property. Gets or sets description of this table"
type: docs
weight: 110
url: /zh/python-net/aspose.words.tables/table/description/
---

## Table.description property

Gets or sets description of this table.
It provides an alternative text representation of the information contained in the table.


```python
@property
def description(self) -> str:
    ...

@description.setter
def description(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents
([OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)).
When saved to pre-ISO/IEC 29500 formats, the property is ignored.




### Examples

Shows how to build a nested table without using a document builder.

```python
doc = aw.Document()
# 创建一个包含三行四列的外部表格，然后将其添加到文档中。
outer_table = ExTable._create_table(doc, 3, 4, 'Outer Table')
doc.first_section.body.append_child(outer_table)
# 创建另一个包含两行两列的表格，然后将其插入到第一个表格的第一个单元格中。
inner_table = ExTable._create_table(doc, 2, 2, 'Inner Table')
outer_table.first_row.first_cell.append_child(inner_table)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateNestedTable.docx')
```

Shows how to build a nested table without using a document builder (CreateTable).

```python
@staticmethod
def _create_table(doc, row_count, cell_count, cell_text):
    table = aw.tables.Table(doc)
    row_id = 1
    while row_id <= row_count:
        row = aw.tables.Row(doc)
        table.append_child(row)
        cell_id = 1
        while cell_id <= cell_count:
            cell = aw.tables.Cell(doc)
            cell.append_child(aw.Paragraph(doc))
            cell.first_paragraph.append_child(aw.Run(doc=doc, text=cell_text))
            row.append_child(cell)
            cell_id += 1
        row_id += 1
    # 您可以使用 "Title" 和 "Description" 属性分别为表格添加标题和描述。
    # 表格必须至少有一行，才能使用这些属性。
    # 这些属性对符合 ISO / IEC 29500 标准的 .docx 文档有意义（参见 OoxmlCompliance 类）。
    # 如果我们将文档保存为 ISO/IEC 29500 之前的格式，Microsoft Word 会忽略这些属性。
    table.title = 'Aspose table title'
    table.description = 'Aspose table description'
    return table
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

