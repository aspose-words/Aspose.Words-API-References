---
title: FieldListNum class
linktitle: FieldListNum class
articleTitle: FieldListNum class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldListNum class. Implements the LISTNUM field"
type: docs
weight: 660
url: /zh/python-net/aspose.words.fields/fieldlistnum/
---

## FieldListNum class

Implements the LISTNUM field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldListNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldListNum()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [has_list_name](./has_list_name/) | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [list_level](./list_level/) | Gets or sets the level in the list, overriding the default behavior of the field. |
| [list_name](./list_name/) | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [starting_number](./starting_number/) | Gets or sets the starting value for this field. |
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

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# LISTNUM 字段显示一个在每个 LISTNUM 字段递增的数字。
# 这些字段还具有多种选项，使我们能够使用它们模拟编号列表。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# 列表默认从 1 开始计数，但我们可以将此数字设置为其他值，例如 0。
# 此字段将显示 "0)"。
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# LISTNUM 字段为每个列表级别维护独立的计数。
# 在同一段落中插入 LISTNUM 字段与另一个 LISTNUM 字段一起
# 会增加列表级别而不是计数。
# 下一个字段将继续我们上面开始的计数，并在列表级别 1 显示值 "1"。
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# 此字段将在列表级别 2 开始计数。它将显示值 "1"。
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# 此字段将在列表级别 3 开始计数。它将显示值 "1"。
# 不同的列表级别有不同的格式，
# 因此，这些字段组合将显示值 "1)a)i)"。
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# 我们插入的下一个 LISTNUM 字段将继续在该列表级别计数
# 即前一个 LISTNUM 字段所在的列表级别。
# 我们可以使用 "ListLevel" 属性跳转到不同的列表级别。
# 如果此 LISTNUM 字段保持在列表级别 3，它将显示 "ii)"，
# 但由于我们已将其移动到列表级别 2，它将在该级别继续计数并显示 "b)"。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# 我们可以设置 ListName 属性，使字段模拟不同的 AUTONUM 字段类型。
# "NumberDefault" 模拟 AUTONUM，"OutlineDefault" 模拟 AUTONUMOUT，
# 并且 "LegalDefault" 模拟 AUTONUMLGL 字段。
# "OutlineDefault" 列表名称以 1 为起始数字将显示 "I."。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# ListName 不会从前一个字段继承，因此我们需要为每个新字段设置它。
# 此字段使用不同的列表名称继续计数并显示 "II."。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

