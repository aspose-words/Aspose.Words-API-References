---
title: DocumentBuilder.move_to_field method
linktitle: move_to_field method
articleTitle: move_to_field method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_field method. Moves the cursor to a field in the document."
type: docs
weight: 570
url: /zh/python-net/aspose.words/documentbuilder/move_to_field/
---

## move_to_field(field, is_after) {#field_bool}

Moves the cursor to a field in the document.


```python
def move_to_field(self, field: aspose.words.fields.Field, is_after: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../../aspose.words.fields/field/) | The field to move the cursor to. |
| is_after | bool | When ``True``, moves the cursor to be after the field end. When ``False``, moves the cursor to be before the field start. |

### Examples

Shows how to move a document builder's node insertion point cursor to a specific field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用 DocumentBuilder 插入字段并在其后添加一段文本。
field = builder.insert_field(field_code=' AUTHOR "John Doe" ')
# 构建器的光标当前位于文档末尾。
self.assertIsNone(builder.current_node)
# 移动光标到字段，同时指定将光标放在字段之前还是之后。
builder.move_to_field(field, move_cursor_to_after_the_field)
# 请注意，在两种情况下光标都位于字段之外。
# 这意味着我们不能这样使用构建器编辑字段。
# 要编辑字段，我们可以在字段的 FieldStart 上使用构建器的 MoveTo 方法
# 或使用 FieldSeparator 节点将光标放置在内部。
if move_cursor_to_after_the_field:
    self.assertIsNone(builder.current_node)
    builder.write(' Text immediately after the field.')
    self.assertEqual('\x13 AUTHOR "John Doe" \x14John Doe\x15 Text immediately after the field.', doc.get_text().strip())
else:
    self.assertEqual(field.start, builder.current_node)
    builder.write('Text immediately before the field. ')
    self.assertEqual('Text immediately before the field. \x13 AUTHOR "John Doe" \x14John Doe\x15', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

