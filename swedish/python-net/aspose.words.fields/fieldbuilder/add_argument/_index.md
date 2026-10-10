---
title: FieldBuilder.add_argument method
linktitle: add_argument method
articleTitle: add_argument method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.add_argument method"
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldbuilder/add_argument/
---

## add_argument(argument) {#str}

Adds a field's argument.


```python
def add_argument(self, argument: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| argument | str | The argument value. |

## add_argument(argument) {#int}

Adds a field's argument.


```python
def add_argument(self, argument: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| argument | int | The argument value. |

## add_argument(argument) {#float}

Adds a field's argument.


```python
def add_argument(self, argument: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| argument | float | The argument value. |

## add_argument(argument) {#fieldbuilder}

Adds a child field represented by another [FieldBuilder](../) to the field's code.



```python
def add_argument(self, argument: aspose.words.fields.FieldBuilder):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| argument | [FieldBuilder](../) |  |

### Remarks

This overload is used when the argument consists of a single child field.


## add_argument(argument) {#fieldargumentbuilder}

Adds a field's argument represented by [FieldArgumentBuilder](../../fieldargumentbuilder/) to the field's code.



```python
def add_argument(self, argument: aspose.words.fields.FieldArgumentBuilder):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| argument | [FieldArgumentBuilder](../../fieldargumentbuilder/) |  |

### Remarks

This overload is used when the argument consists of a mixture of different parts such as child fields, nodes, and plain text.


## Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
from aspose.words.fields import FieldType, FieldBuilder, FieldArgumentBuilder
doc = aw.Document()
# Nedan följer tre exempel på fältkonstruktion gjorda med en fältbyggare.
# 1 -  Enstaka fält:
# Använd en fältbyggare för att lägga till ett SYMBOL-fält som visar ƒ (Florin)-symbolen.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Nästlat fält:
# Använd en fältbyggare för att skapa ett formelfält som används som ett inre fält av en annan fältbyggare.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Skapa en annan byggare för ett annat SYMBOL-fält och infoga formelfältet
# som vi har skapat ovan i SYMBOL-fältet som dess argument.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Det yttre SYMBOL-fältet kommer att använda formelfältets resultat, 174, som dess argument,
# vilket får fältet att visa ® (Registrerad symbol) eftersom dess teckennummer är 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Flera nästlade fält och argument:
# Nu kommer vi att använda en byggare för att skapa ett IF-fält, som visar ett av två anpassade strängvärden,
# beroende på sant/falskt-värdet av dess uttryck. För att få ett sant/falskt värde
# som bestämmer vilken sträng IF-fältet visar, kommer IF-fältet att testa två numeriska uttryck för likhet.
# Vi kommer att tillhandahålla de två uttrycken i form av formelfält, som vi kommer att nästla inuti IF-fältet.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Nästa steg är att bygga två fältargument, som kommer att fungera som sant/falskt-utdatasträngar för IF-fältet.
# Dessa argument kommer att återanvända utdatavärdena från våra numeriska uttryck.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Slutligen kommer vi att skapa en ytterligare fältbyggare för IF-fältet och kombinera alla uttryck.
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

