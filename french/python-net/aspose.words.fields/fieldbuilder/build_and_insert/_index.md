---
title: FieldBuilder.build_and_insert method
linktitle: build_and_insert method
articleTitle: build_and_insert method
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldBuilder.build_and_insert method"
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/fieldbuilder/build_and_insert/
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
# Une façon pratique d'ajouter du texte à un document est d'utiliser un constructeur de document.
builder = aw.DocumentBuilder(doc)
builder.write(' Hello world! This text is one Run, which is an inline node.')
# Les champs ont leur constructeur, que nous pouvons utiliser pour construire le code du champ morceau par morceau.
# Dans ce cas, nous allons construire un champ BARCODE représentant un code postal américain,
# et l'insérer ensuite devant un Run.
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

