---
title: FieldEmbed class
linktitle: FieldEmbed class
articleTitle: FieldEmbed class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldEmbed class. Implements the EMBED field"
type: docs
weight: 390
url: /zh/python-net/aspose.words.fields/fieldembed/
---

## FieldEmbed class

Implements the EMBED field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldEmbed](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldEmbed()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# 打开一个在 Microsoft Word 2003 中创建的文档。
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# 如果我们打开 Word 文档并按 Alt+F9，就会看到一个 SHAPE 字段和一个 EMBED 字段。
# SHAPE 字段是带有“与文字同行”换行样式的 AutoShape 对象的锚点/画布。
# EMBED 字段具有相同的功能，但用于嵌入的对象，
# 例如来自外部 Excel 文档的电子表格。
# 然而，这些字段不会出现在文档的 Fields 集合中。
self.assertEqual(0, doc.range.fields.count)
# 这些字段仅在旧版本的 Microsoft Word 中受支持。
# 文档加载过程会将这些字段转换为 Shape 对象，
# 我们可以在文档的节点集合中访问它们。
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# 第一个 Shape 节点对应于输入文档中的 SHAPE 字段，
# 它是 AutoShape 的行内画布。
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# 第二个 Shape 节点就是 AutoShape 本身。
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# 第三个 Shape 是原先包含外部电子表格的 EMBED 字段。
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

