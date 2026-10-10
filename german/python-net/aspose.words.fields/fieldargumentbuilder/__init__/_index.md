---
title: FieldArgumentBuilder constructor
linktitle: FieldArgumentBuilder constructor
articleTitle: FieldArgumentBuilder constructor
second_title: Aspose.Words for Python
description: "FieldArgumentBuilder constructor. Initializes an instance of the [FieldArgumentBuilder](../) class."
type: docs
weight: 10
url: /de/python-net/aspose.words.fields/fieldargumentbuilder/__init__/
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
# Unten sind drei Beispiele für die Feldkonstruktion mit einem Feld-Builder.
# 1 -  Einzelnes Feld:
# Verwenden Sie einen Feld-Builder, um ein SYMBOL-Feld hinzuzufügen, das das ƒ (Florin)-Symbol anzeigt.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=402)
builder.add_switch(switch_name='\\f', switch_argument='Arial')
builder.add_switch(switch_name='\\s', switch_argument=25)
builder.add_switch(switch_name='\\u')
field = builder.build_and_insert(ref_node=doc.first_section.body.first_paragraph)
self.assertEqual(' SYMBOL 402 \\f Arial \\s 25 \\u ', field.get_field_code())
# 2 -  Verschachteltes Feld:
# Verwenden Sie einen Feld-Builder, um ein Formelfeld zu erstellen, das von einem anderen Feld-Builder als inneres Feld verwendet wird.
inner_formula_builder = FieldBuilder(FieldType.FIELD_FORMULA)
inner_formula_builder.add_argument(argument=100)
inner_formula_builder.add_argument(argument='+')
inner_formula_builder.add_argument(argument=74)
# Erstellen Sie einen weiteren Builder für ein weiteres SYMBOL-Feld und fügen Sie das Formelfeld ein
# das wir oben erstellt haben, in das SYMBOL-Feld als Argument ein.
builder = FieldBuilder(FieldType.FIELD_SYMBOL)
builder.add_argument(argument=inner_formula_builder)
field = builder.build_and_insert(ref_node=doc.first_section.body.append_paragraph(''))
# Das äußere SYMBOL-Feld wird das Ergebnis des Formelfelds, 174, als Argument verwenden,
# was dazu führt, dass das Feld das ® (Registriertes Zeichen)-Symbol anzeigt, da seine Zeichen‑Nummer 174 ist.
self.assertEqual(' SYMBOL \x13 = 100 + 74 \x14\x15 ', field.get_field_code())
# 3 -  Mehrere verschachtelte Felder und Argumente:
# Jetzt werden wir einen Builder verwenden, um ein IF‑Feld zu erstellen, das einen von zwei benutzerdefinierten Zeichenkettenwerten anzeigt,
# abhängig vom Wahr/Falsch‑Wert seines Ausdrucks. Um einen Wahr/Falsch‑Wert zu erhalten
# der bestimmt, welche Zeichenkette das IF‑Feld anzeigt, wird das IF‑Feld zwei numerische Ausdrücke auf Gleichheit prüfen.
# Wir werden die beiden Ausdrücke in Form von Formelfeldern bereitstellen, die wir innerhalb des IF‑Feldes verschachteln.
left_expression = FieldBuilder(FieldType.FIELD_FORMULA)
left_expression.add_argument(argument=2)
left_expression.add_argument(argument='+')
left_expression.add_argument(argument=3)
right_expression = FieldBuilder(FieldType.FIELD_FORMULA)
right_expression.add_argument(argument=2.5)
right_expression.add_argument(argument='*')
right_expression.add_argument(argument=5.2)
# Als Nächstes werden wir zwei Feldargumente erstellen, die als Wahr/Falsch‑Ausgabezeichenketten für das IF‑Feld dienen.
# Diese Argumente werden die Ausgabewerte unserer numerischen Ausdrücke wiederverwenden.
true_output = FieldArgumentBuilder()
true_output.add_text('True, both expressions amount to ')
true_output.add_field(left_expression)
false_output = FieldArgumentBuilder()
false_output.add_node(aw.Run(doc=doc, text='False, '))
false_output.add_field(left_expression)
false_output.add_node(aw.Run(doc=doc, text=' does not equal '))
false_output.add_field(right_expression)
# Schließlich werden wir einen weiteren Feld-Builder für das IF‑Feld erstellen und alle Ausdrücke kombinieren.
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

