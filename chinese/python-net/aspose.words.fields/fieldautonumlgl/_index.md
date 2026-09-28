---
title: FieldAutoNumLgl class
linktitle: FieldAutoNumLgl class
articleTitle: FieldAutoNumLgl class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldAutoNumLgl class. Implements the AUTONUMLGL field"
type: docs
weight: 130
url: /zh/python-net/aspose.words.fields/fieldautonumlgl/
---

## FieldAutoNumLgl class

Implements the AUTONUMLGL field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts an automatic number in legal format.


**Inheritance:** [FieldAutoNumLgl](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAutoNumLgl()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [remove_trailing_period](./remove_trailing_period/) | Gets or sets whether to display the number without a trailing period. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [separator_character](./separator_character/) | Gets or sets the separator character to be used. |
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

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# AUTONUMLGL 字段显示一个数字，该数字在当前标题级别的每个 AUTONUMLGL 字段处递增。
# 这些字段为每个标题级别维护一个单独的计数，
# 并且每个字段还显示其自身以下所有标题级别的 AUTONUMLGL 字段计数。
# 更改任何标题级别的计数会将该级别以上所有级别的计数重置为 1。
# 这使我们能够以大纲列表的形式组织文档。
# 这是在标题级别 1 的第一个 AUTONUMLGL 字段，在文档中显示 “1.”。
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# 这是在标题级别 1 的第二个 AUTONUMLGL 字段，因此它将显示 “2.”。
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# 这是在标题级别 2 的第一个 AUTONUMLGL 字段，
# 而其下一级标题的 AUTONUMLGL 计数为 “2”，因此它将显示 “2.1.”。
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# 这是在标题级别 3 的第一个 AUTONUMLGL 字段。
# 以与上面的字段相同的方式工作，它将显示 “2.1.1.”。
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# 此字段位于标题级别 2，其相应的 AUTONUMLGL 计数为 2，因此该字段将显示 “2.2.”。
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# 为该级别以下的标题级别递增 AUTONUMLGL 计数
# 已将此级别的计数重置，使该字段显示 “2.2.1.”。
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # 分隔符字符会紧跟在字段结果的数字后出现，
    # 默认情况下是句点。如果我们将此属性设为 null，
    # 我们最后的 AUTONUMLGL 字段将在文档中显示 “2.2.1.”。
    self.assertIsNone(field.separator_character)
    # 设置自定义分隔符字符并移除结尾的句点
    # 将把该字段的外观从 “2.2.1.” 更改为 “2:2:1”。
    # 我们将把此应用于所有已创建的字段。
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # 此文本将属于其上方的自动编号法律字段。
    # 当我们点击 Microsoft Word 中相应 AUTONUMLGL 字段旁边的箭头时，它将折叠。
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

