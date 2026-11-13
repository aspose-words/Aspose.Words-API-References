---
title: FieldBuilder.build_and_insert method
linktitle: build_and_insert method
articleTitle: build_and_insert method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.build_and_insert method"
type: docs
weight: 40
url: /es/python-net/aspose.words.fields/fieldbuilder/build_and_insert/
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
# Una forma conveniente de añadir contenido de texto a un documento es con un document builder.
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# Los campos tienen su builder, que podemos usar para construir el código del campo pieza a pieza.
# En este caso, construiremos un campo BARCODE que representa un código postal de EE. UU.,
# y luego lo insertaremos delante de un Run.
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

