---
title: FieldEQ class
linktitle: FieldEQ class
articleTitle: FieldEQ class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldEQ class. Implements the EQ field"
type: docs
weight: 370
url: /zh/python-net/aspose.words.fields/fieldeq/
---

## FieldEQ class

Implements the EQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldEQ](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldEQ()](./__init__/#default) | The default constructor. |

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
|[ as_office_math()](./as_office_math/#default) | Returns Office Math object corresponded to the EQ field. |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use the EQ field to display a variety of mathematical equations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# EQ 字段显示由一个或多个元素组成的数学公式。
# 每个元素采用以下形式：[switch][options][arguments]。
# 可能只有一个 switch，且有多个可选的 options。
# 参数是一组用圆括号括起来的逗号分隔值。
# 这里我们使用文档生成器插入一个 EQ 字段，使用 "\\f" switch，对应于 “Fraction”。
# 我们将传入值 1 和 4 作为参数，并且不使用任何 options。
# 该字段将显示一个分数，分子为 1，分母为 4。
field = ExField._insert_field_eq(builder, '\\f(1,4)')
self.assertEqual(' EQ \\f(1,4)', field.get_field_code())
# 一个 EQ 字段可以包含按顺序放置的多个元素。
# 我们还可以通过将内部元素放置在
# 外部元素的参数括号内来嵌套元素。
# 我们可以在此处找到完整的 switch 列表及其用法：
# https:#blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/
# 下面列出了九个不同的 EQ field switch 的应用示例，可用于创建不同类型的对象。
# 1 -  数组切换 "\a"，左对齐，2 列，水平和垂直间距为 3 点：
ExField._insert_field_eq(builder, '\\a \\al \\co2 \\vs3 \\hs3(4x,- 4y,-4x,+ y)')
# 2 -  括号切换 "\b"，括号字符 "["，用于将内容包裹在一对方括号中：
# 请注意，我们在括号内嵌套了一个数组，输出时整体看起来像一个矩阵。
ExField._insert_field_eq(builder, '\\b \\bc\\[ (\\a \\al \\co3 \\vs3 \\hs3(1,0,0,0,1,0,0,0,1))')
# 3 -  位移切换 "\d"，将文本 "B" 向右移动 30 个空格相对于 "A"，并将间距显示为下划线：
ExField._insert_field_eq(builder, 'A \\d \\fo30 \\li() B')
# 4 -  包含多个分数的公式：
ExField._insert_field_eq(builder, '\\f(d,dx)(u + v) = \\f(du,dx) + \\f(dv,dx)')
# 5 -  积分切换 "\i"，带有求和符号：
ExField._insert_field_eq(builder, '\\i \\su(n=1,5,n)')
# 6 -  列表切换 "\l"：
ExField._insert_field_eq(builder, '\\l(1,1,2,3,n,8,13)')
# 7 -  根号切换 "\r"，显示 x 的三次方根：
ExField._insert_field_eq(builder, '\\r (3,x)')
# 8 -  下标/上标切换 "/s"，先作为上标再作为下标：
ExField._insert_field_eq(builder, '\\s \\up8(Superscript) Text \\s \\do8(Subscript)')
# 9 -  框线切换 "\x"，在输入的顶部、底部、左侧和右侧添加线条：
ExField._insert_field_eq(builder, '\\x \\to \\bo \\le \\ri(5)')
# 一些更复杂的组合。
ExField._insert_field_eq(builder, '\\a \\ac \\vs1 \\co1(lim,n→∞) \\b (\\f(n,n2 + 12) + \\f(n,n2 + 22) + ... + \\f(n,n2 + n2))')
ExField._insert_field_eq(builder, '\\i (,,  \\b(\\f(x,x2 + 3x + 2))) \\s \\up10(2)')
ExField._insert_field_eq(builder, '\\i \\in( tan x, \\s \\up2(sec x), \\b(\\r(3) )\\s \\up4(t) \\s \\up7(2)  dt)')
doc.save(file_name=ARTIFACTS_DIR + 'Field.EQ.docx')
```

Shows how to use the EQ field to display a variety of mathematical equations (InsertFieldEQ).

```python
@staticmethod
def _insert_field_eq(builder, args):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_EQUATION, update_field=True).as_field_eq()
    builder.move_to(field.separator)
    builder.write(args)
    builder.move_to(field.start.parent_node)
    builder.insert_paragraph()
    return field
```

Shows how to replace the EQ field with Office Math.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - EQ.docx')
field_eq = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_field_eq(), b), list(doc.range.fields))))[0]
office_math = field_eq.as_office_math()
field_eq.start.parent_node.insert_before(office_math, field_eq.start)
field_eq.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Field.EQAsOfficeMath.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

