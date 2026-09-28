---
title: NodeCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "NodeCollection.count property. Gets the number of nodes in the collection."
type: docs
weight: 20
url: /zh/python-net/aspose.words/nodecollection/count/
---

## NodeCollection.count property

Gets the number of nodes in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# 向本文档的第一段添加两个运行（run）和一个形状作为子节点。
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# 请注意，'CustomNodeId' 不会保存到输出文件中，仅在节点生命周期内存在。
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# 遍历段落的直接子项集合，
# 并打印我们在其中找到的任何运行或形状。
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    switch_condition = child.node_type
    if switch_condition == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif switch_condition == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

Shows how to find out if a tables are nested.

```python
doc = aw.Document(file_name=MY_DIR + 'Nested tables.docx')
tables = doc.get_child_nodes(aw.NodeType.TABLE, True)
i = 0
while i < tables.count:
    table = tables[i].as_table()
    # 找出表格中的任何单元格是否包含其他表格作为子项。
    count = ExTable._get_child_table_count(table)
    print('Table #{0} has {1} tables directly within its cells'.format(i, count))
    # 找出该表格是否嵌套在另一个表格中，如果是，嵌套的深度是多少。
    table_depth = ExTable._get_nested_depth_of_table(table)
    if table_depth > 0:
        print('Table #{0} is nested inside another table at depth of {1}'.format(i, table_depth))
    else:
        print('Table #{0} is a non nested table (is not a child of another table)'.format(i))
    i += 1
```

Shows how to find out if a tables are nested (GetNestedDepthOfTable).

```python
@staticmethod
def _get_nested_depth_of_table(table):
    depth = 0
    parent = table.get_ancestor(aw.tables.Table)
    while parent is not None:
        depth += 1
        parent = parent.get_ancestor(aw.tables.Table)
    return depth

@staticmethod
def _get_child_table_count(table):
    child_table_count = 0
    for row in table.rows:
        row = row.as_row()
        for cell in row.cells:
            cell = cell.as_cell()
            child_tables = cell.tables
            if child_tables.count > 0:
                child_table_count += 1
    return child_table_count
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

