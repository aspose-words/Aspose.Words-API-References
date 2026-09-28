---
title: EditableRange.editor_group property
linktitle: editor_group property
articleTitle: editor_group property
second_title: Aspose.Words for Python
description: "EditableRange.editor_group property. Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range."
type: docs
weight: 30
url: /zh/python-net/aspose.words/editablerange/editor_group/
---

## EditableRange.editor_group property

Returns or sets an alias (or editing group) which shall be used to determine if the current user
shall be allowed to edit this editable range.


```python
@property
def editor_group(self) -> aspose.words.EditorType:
    ...

@editor_group.setter
def editor_group(self, value: aspose.words.EditorType):
    ...

```

### Remarks

Single user and editor group cannot be set simultaneously for the specific editable range,
if the one is set, the other will be clear.




### Examples

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
* class [EditableRange](../)

