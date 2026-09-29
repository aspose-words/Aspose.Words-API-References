---
title: FieldArgumentBuilder constructor
linktitle: FieldArgumentBuilder constructor
articleTitle: FieldArgumentBuilder constructor
second_title: Aspose.Words for Python
description: "FieldArgumentBuilder constructor. Initializes an instance of the [FieldArgumentBuilder](../) class."
type: docs
weight: 10
url: /it/python-net/aspose.words.fields/fieldargumentbuilder/__init__/
---

## FieldArgumentBuilder() {#default}

Initializes an instance of the [FieldArgumentBuilder](../) class.



```python
def __init__(self):
    ...
```

### Examples

Shows how to construct fields using a field builder, and then insert them into the document.

```python
from api_example_base import ApiExampleBase, ARTIFACTS_DIR
import aspose.words as aw
from aspose.words.fields import FieldType, FieldBuilder, FieldArgumentBuilder
doc = aw.Document()
# Di seguito sono riportati tre esempi di costruzione di campi eseguiti usando un costruttore di campi.
# 1 -  Campo singolo:
# Usa un costruttore di campi per aggiungere un campo SYMBOL che visualizza il simbolo ƒ (Fiorino).
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Campo annidato:
# Usa un costruttore di campi per creare un campo formula usato come campo interno da un altro costruttore di campi.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Crea un altro costruttore per un altro campo SYMBOL e inserisci il campo formula
# che abbiamo creato sopra nel campo SYMBOL come suo argomento.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Il campo SYMBOL esterno utilizzerà il risultato del campo formula, 174, come suo argomento,
# il che farà visualizzare al campo il simbolo ® (Segno di registrazione) poiché il suo numero di carattere è 174.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Campi annidati multipli e argomenti:
# Ora, utilizzeremo un costruttore per creare un campo IF, che visualizza uno dei due valori di stringa personalizzati,
# in base al valore vero/falso della sua espressione. Per ottenere un valore vero/falso
# che determina quale stringa visualizza il campo IF, il campo IF testerà due espressioni numeriche per uguaglianza.
# Forniremo le due espressioni sotto forma di campi formula, che annideremo all'interno del campo IF.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Successivamente, costruiremo due argomenti di campo, che serviranno come stringhe di output vero/falso per il campo IF.
# Questi argomenti riutilizzeranno i valori di output delle nostre espressioni numeriche.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Infine, creeremo un altro costruttore di campi per il campo IF e combineremo tutte le espressioni.
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

### See Also

* module [aspose.words.fields](../../)
* class [FieldArgumentBuilder](../)

