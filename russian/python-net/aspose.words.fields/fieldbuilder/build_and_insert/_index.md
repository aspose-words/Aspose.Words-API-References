---
title: FieldBuilder.build_and_insert method
linktitle: build_and_insert method
articleTitle: build_and_insert method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.build_and_insert method"
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/fieldbuilder/build_and_insert/
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
# Удобный способ добавить текстовое содержимое в документ — использовать построитель документов.
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# У полей есть свой построитель, который мы можем использовать для пошагового построения кода поля.
# В этом случае мы создадим поле BARCODE, представляющее почтовый индекс США,
# а затем вставим его перед Run.
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
# Ниже приведены три примера построения полей с использованием построителя полей.
# 1 -  Одинарное поле:
# Используйте построитель полей, чтобы добавить поле SYMBOL, которое отображает символ ƒ (флорин).
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Вложенное поле:
# Используйте построитель полей, чтобы создать поле формулы, используемое как вложенное поле другим построителем полей.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Создайте еще один построитель для другого поля SYMBOL и вставьте поле формулы
# которое мы создали выше, в поле SYMBOL в качестве его аргумента.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Внешнее поле SYMBOL будет использовать результат поля формулы, 174, в качестве своего аргумента,
# что заставит поле отображать символ ® (знак регистрации), поскольку его номер символа — 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Несколько вложенных полей и аргументов:
# Теперь мы используем построитель, чтобы создать поле IF, которое отображает одну из двух пользовательских строковых значений,
# в зависимости от истинного/ложного значения его выражения. Чтобы получить истинное/ложное значение
# которое определяет, какую строку отображает поле IF, поле IF проверит два числовых выражения на равенство.
# Мы предоставим два выражения в виде полей формулы, которые вложим внутрь поля IF.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Далее мы создадим два аргумента поля, которые будут служить строками вывода истинного/ложного значения для поля IF.
# Эти аргументы будут повторно использовать выходные значения наших числовых выражений.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Наконец, мы создадим еще один построитель полей для поля IF и объединим все выражения.
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

