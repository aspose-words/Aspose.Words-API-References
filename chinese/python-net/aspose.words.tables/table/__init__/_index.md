---
title: Table constructor
linktitle: Table constructor
articleTitle: Table constructor
second_title: Aspose.Words for Python
description: "Table constructor. Initializes a new instance of the [Table](../) class."
type: docs
weight: 10
url: /zh/python-net/aspose.words.tables/table/__init__/
---

## Table(doc) {#documentbase}

Initializes a new instance of the [Table](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |

### Remarks

When [Table](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../../aspose.words/node/parent_node/) is ``None``.

To append [Table](../) to the document use [CompositeNode.insert_after()](../../../aspose.words/compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../../aspose.words/compositenode/insert_before/#node_node)
on the story where you want the table inserted.




### Examples

Shows how to create a table.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
# 表格包含行，行包含单元格，单元格可能包含段落
# 其中常见的元素包括文本运行、形状，甚至其他表格。
# 在表格上调用 "EnsureMinimum" 方法将确保
# 该表格至少拥有一行、一个单元格和一个段落。
first_row = aw.tables.Row(doc)
table.append_child(first_row)
first_cell = aw.tables.Cell(doc)
first_row.append_child(first_cell)
paragraph = aw.Paragraph(doc)
first_cell.append_child(paragraph)
# 向表格第一行的第一个单元格添加文本。
run = aw.Run(doc=doc, text='Hello world!')
paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Table.CreateTable.docx')
```

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

