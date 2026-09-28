---
title: EditableRangeEnd.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "EditableRangeEnd.node_type property. Returns [NodeType.EDITABLE_RANGE_END](../../nodetype/#EDITABLE_RANGE_END)."
type: docs
weight: 30
url: /zh/python-net/aspose.words/editablerangeend/node_type/
---

## EditableRangeEnd.node_type property

Returns [NodeType.EDITABLE_RANGE_END](../../nodetype/#EDITABLE_RANGE_END).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# 可编辑范围允许我们在受保护文档中保留可编辑的部分。
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# 一个结构良好的可编辑范围具有起始节点和结束节点。
# 这些节点具有匹配的 ID，并包含可编辑节点。
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# 可编辑范围的不同部分相互链接。
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# 我们可以这样访问每个部分的节点类型。可编辑范围本身不是节点，
# 而是由起始、结束以及它们包含的内容组成的实体。
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# 移除可编辑范围。范围内的所有节点将保持完整。
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRangeEnd](../)

