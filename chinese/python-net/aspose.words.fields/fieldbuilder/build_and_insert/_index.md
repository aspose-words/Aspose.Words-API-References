---
title: FieldBuilder.build_and_insert method
linktitle: build_and_insert method
articleTitle: build_and_insert method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.build_and_insert method"
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldbuilder/build_and_insert/
---

## build_and_insert(ref_node) {#inline}

Builds and inserts a field into the document before the specified inline node.


```python
def build_and_insert(self, ref_node: aspose.words.Inline):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ref_node | [Inline](../../../aspose.words/inline/) |  |

### Returns

A [Field](../../field/) object that represents the inserted field.


## build_and_insert(ref_node) {#paragraph}

Builds and inserts a field into the document to the end of the specified paragraph.


```python
def build_and_insert(self, ref_node: aspose.words.Paragraph):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ref_node | [Paragraph](../../../aspose.words/paragraph/) |  |

### Returns

A [Field](../../field/) object that represents the inserted field.


## Examples

Shows how to create and insert a field using a field builder.

```python
doc = aw.Document()
# 向文档添加文本内容的便捷方法是使用文档生成器。
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# 字段拥有各自的生成器，我们可以用它逐步构建字段代码。
# 在本例中，我们将构建一个表示美国邮政编码的 BARCODE 字段，
# 然后将其插入到一个 Run 前面。
field_builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_BARCODE)
field_builder.add_argument('90210')
field_builder.add_switch('\\f', 'A')
field_builder.add_switch('\\u')
field_builder.build_and_insert(doc.first_section.body.first_paragraph.runs[0])
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.create_with_field_builder.docx')
```

Shows how to construct fields using a field builder, and then insert them into the document.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
from aspose.words.fields import FieldType, FieldBuilder, FieldArgumentBuilder
doc = aw.Document()
# 以下是使用字段构建器完成的三个字段构建示例。
# 1 -  单字段：
# 使用字段构建器添加一个显示 ƒ（弗林）符号的 SYMBOL 字段。
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  嵌套字段：
# 使用字段构建器创建一个由另一个字段构建器用作内部字段的公式字段。
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# 为另一个 SYMBOL 字段创建另一个构建器，并插入公式字段
# 我们在上面创建的公式字段作为参数插入到 SYMBOL 字段中。
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# 外部的 SYMBOL 字段将使用公式字段的结果 174 作为其参数，
# 由于其字符编号为 174，这将使字段显示 ®（注册商标）符号。
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  多个嵌套字段和参数：
# 现在，我们将使用构建器创建一个 IF 字段，该字段显示两个自定义字符串值之一，
# 取决于其表达式的真/假值。为了获得真/假值
# 决定 IF 字段显示哪个字符串，IF 字段将测试两个数值表达式是否相等。
# 我们将以公式字段的形式提供这两个表达式，并将其嵌套在 IF 字段内部。
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# 接下来，我们将构建两个字段参数，作为 IF 字段的真/假输出字符串。
# 这些参数将复用我们数值表达式的输出值。
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# 最后，我们将为 IF 字段再创建一个字段构建器，并组合所有表达式。
builder = FieldBuilder(FieldType.FIELD_IF)
builder.add_argument(argument=left_expression)
builder.add_argument(argument='=')
builder.add_argument(argument=right_expression)
builder.add_argument(argument=true_output)
builder.add_argument(argument=false_output)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
self.assertEqual(' IF \x13 = 2 + 3 \x14\x15 = \x13 = 2.5 * 5.2 \x14\x15 ' + '"True, both expressions amount to \x13 = 2 + 3 \x14\x15" ' + '"False, \x13 = 2 + 3 \x14\x15 does not equal \x13 = 2.5 * 5.2 \x14\x15" ', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SYMBOL.docx')
```

## See Also

* module [aspose.words.fields](../../)
* class [FieldBuilder](../)

