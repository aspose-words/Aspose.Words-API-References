---
title: FieldArgumentBuilder class
linktitle: FieldArgumentBuilder class
articleTitle: FieldArgumentBuilder class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldArgumentBuilder class. Builds a complex field argument consisting of fields, nodes, and plain text"
type: docs
weight: 90
url: /python-net/aspose.words.fields/fieldargumentbuilder/
---

## FieldArgumentBuilder class

Builds a complex field argument consisting of fields, nodes, and plain text.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [FieldArgumentBuilder()](./__init__/#default) | Initializes an instance of the [FieldArgumentBuilder](./) class. |

### Methods

| Name | Description |
| --- | --- |
|[ add_field(field_builder)](./add_field/#fieldbuilder) | Adds a field represented by a [FieldBuilder](../fieldbuilder/) to the argument. |
|[ add_node(node)](./add_node/#inline) | Adds a node to the argument. |
|[ add_text(text)](./add_text/#str) | Adds a plain text to the argument. |

### Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```python
doc = aw.Document()
# Below are three examples of field construction done using a field builder.
# 1 -  Single field:
# Use a field builder to add a SYMBOL field which displays the ƒ (Florin) symbol.
builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Nested field:
# Use a field builder to create a formula field used as an inner field by another field builder.
inner_formula_builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Create another builder for another SYMBOL field, and insert the formula field
# that we have created above into the SYMBOL field as its argument.
builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# The outer SYMBOL field will use the formula field result, 174, as its argument,
# which will make the field display the ® (Registered Sign) symbol since its character number is 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Multiple nested fields and arguments:
# Now, we will use a builder to create an IF field, which displays one of two custom string values,
# depending on the true/false value of its expression. To get a true/false value
# that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
# We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
left_expression = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
# These arguments will reuse the output values of our numeric expressions.
true_output = aw.fields.FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = aw.fields.FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Finally, we will create one more field builder for the IF field and combine all of the expressions.
builder = aw.fields.FieldBuilder(aw.fields.FieldType.FIELD_IF)
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

### See Also

* module [aspose.words.fields](../)

