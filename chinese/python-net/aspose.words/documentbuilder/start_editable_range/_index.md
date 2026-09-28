---
title: DocumentBuilder.start_editable_range method
linktitle: start_editable_range method
articleTitle: start_editable_range method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_editable_range method. Marks the current position in the document as an editable range start."
type: docs
weight: 670
url: /zh/python-net/aspose.words/documentbuilder/start_editable_range/
---

## start_editable_range() {#default}

Marks the current position in the document as an editable range start.


```python
def start_editable_range(self):
    ...
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](./#default) and [DocumentBuilder.end_editable_range()](../end_editable_range/#default)
or [DocumentBuilder.end_editable_range()](../end_editable_range/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


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

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " + 'we cannot edit this paragraph without the password.')
# 创建两个嵌套的可编辑范围。
outer_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside the outer editable range and can be edited.')
inner_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside both the outer and inner editable ranges and can be edited.')
# 当前，文档构建器的节点插入光标位于多个正在进行的可编辑范围内。
# 当我们想在这种情况下结束可编辑范围时，
# 需要通过传递其 EditableRangeStart 节点来指定要结束的范围。
builder.end_editable_range(inner_editable_range_start)
builder.writeln('This paragraph inside the outer editable range and can be edited.')
builder.end_editable_range(outer_editable_range_start)
builder.writeln('This paragraph is outside any editable ranges, and cannot be edited.')
# 如果一段文本具有两个具有指定组的重叠可编辑范围，
# 那么两个组共同排除的用户组将被阻止编辑该文本。
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.Nested.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

