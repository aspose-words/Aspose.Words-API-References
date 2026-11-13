---
title: FieldBuilder.add_argument method
linktitle: add_argument method
articleTitle: add_argument method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.add_argument method"
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldbuilder/add_argument/
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
# A continuación se presentan tres ejemplos de construcción de campos realizados con un generador de campos.
# 1 -  Campo único:
# Utilice un generador de campos para agregar un campo SYMBOL que muestra el símbolo ƒ (Florín).
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Campo anidado:
# Utilice un generador de campos para crear un campo de fórmula que se usa como campo interno por otro generador de campos.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Cree otro generador para otro campo SYMBOL y inserte el campo de fórmula
# que hemos creado arriba en el campo SYMBOL como su argumento.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# El campo SYMBOL externo usará el resultado del campo de fórmula, 174, como su argumento,
# lo que hará que el campo muestre el símbolo ® (Marca registrada) ya que su número de carácter es 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Múltiples campos anidados y argumentos:
# Ahora, utilizaremos un generador para crear un campo IF, que muestra uno de dos valores de cadena personalizados,
# dependiendo del valor verdadero/falso de su expresión. Para obtener un valor verdadero/falso
# que determina qué cadena muestra el campo IF, el campo IF probará dos expresiones numéricas para igualdad.
# Proporcionaremos las dos expresiones en forma de campos de fórmula, que anidaremos dentro del campo IF.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# A continuación, construiremos dos argumentos de campo, que servirán como cadenas de salida verdadero/falso para el campo IF.
# Estos argumentos reutilizarán los valores de salida de nuestras expresiones numéricas.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Finalmente, crearemos un generador de campo más para el campo IF y combinaremos todas las expresiones.
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

