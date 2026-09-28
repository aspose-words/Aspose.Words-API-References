---
title: FieldBuilder.add_switch method
linktitle: add_switch method
articleTitle: add_switch method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.add_switch method"
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldbuilder/add_switch/
---

## add_switch(switch_name) {#str}

Adds a field's switch.


```python
def add_switch(self, switch_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switch_name | str | The switch name. |

### Remarks

This overload adds a flag (switch without argument).


## add_switch(switch_name, switch_argument) {#str_str}

Adds a field's switch.


```python
def add_switch(self, switch_name: str, switch_argument: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switch_name | str | The switch name. |
| switch_argument | str | The switch value. |

## add_switch(switch_name, switch_argument) {#str_int}

Adds a field's switch.


```python
def add_switch(self, switch_name: str, switch_argument: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switch_name | str | The switch name. |
| switch_argument | int | The switch value. |

## add_switch(switch_name, switch_argument) {#str_float}

Adds a field's switch.


```python
def add_switch(self, switch_name: str, switch_argument: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switch_name | str | The switch name. |
| switch_argument | float | The switch value. |

## Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
from aspose.words.fields import FieldType, FieldBuilder, FieldArgumentBuilder
doc = aw.Document()
# Voici trois exemples de construction de champ réalisés à l'aide d'un constructeur de champ.
# 1 -  Champ unique :
# Utilisez un constructeur de champ pour ajouter un champ SYMBOL qui affiche le symbole ƒ (Florin).
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Champ imbriqué :
# Utilisez un constructeur de champ pour créer un champ de formule utilisé comme champ interne par un autre constructeur de champ.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Créez un autre constructeur pour un autre champ SYMBOL, et insérez le champ de formule
# que nous avons créé ci-dessus dans le champ SYMBOL comme son argument.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Le champ SYMBOL externe utilisera le résultat du champ de formule, 174, comme son argument,
# ce qui fera afficher au champ le symbole ® (Signe enregistré) puisque son numéro de caractère est 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Champs imbriqués multiples et arguments :
# Maintenant, nous utiliserons un constructeur pour créer un champ IF, qui affiche l'une des deux valeurs de chaîne personnalisées,
# en fonction de la valeur vrai/faux de son expression. Pour obtenir une valeur vrai/faux
# qui détermine quelle chaîne le champ IF affiche, le champ IF testera deux expressions numériques pour l'égalité.
# Nous fournirons les deux expressions sous forme de champs de formule, que nous imbriquerons à l'intérieur du champ IF.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Ensuite, nous construirons deux arguments de champ, qui serviront de chaînes de sortie vrai/faux pour le champ IF.
# Ces arguments réutiliseront les valeurs de sortie de nos expressions numériques.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Enfin, nous créerons un autre constructeur de champ pour le champ IF et combinerons toutes les expressions.
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

