---
title: FieldAutoNumLgl.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 30
url: /it/python-net/aspose.words.fields/fieldautonumlgl/separator_character/
---

## FieldAutoNumLgl.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# I campi AUTONUMLGL mostrano un numero che incrementa ad ogni campo AUTONUMLGL all'interno del suo attuale livello di intestazione.
# Questi campi mantengono un conteggio separato per ogni livello di intestazione,
# e ogni campo mostra anche i conteggi dei campi AUTONUMLGL per tutti i livelli di intestazione inferiori al proprio.
# Modificare il conteggio per qualsiasi livello di intestazione ripristina i conteggi per tutti i livelli superiori a quello a 1.
# Ciò ci consente di organizzare il nostro documento sotto forma di elenco strutturato.
# Questo è il primo campo AUTONUMLGL a un livello di intestazione 1, visualizza "1." nel documento.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Questo è il secondo campo AUTONUMLGL a un livello di intestazione 1, quindi visualizzerà "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Questo è il primo campo AUTONUMLGL a un livello di intestazione 2,
# e il conteggio AUTONUMLGL per il livello di intestazione inferiore è "2", quindi visualizzerà "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Questo è il primo campo AUTONUMLGL a un livello di intestazione 3.
# Funzionando nello stesso modo del campo sopra, visualizzerà "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Questo campo è a un livello di intestazione 2, e il relativo conteggio AUTONUMLGL è 2, quindi il campo visualizzerà "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Incrementare il conteggio AUTONUMLGL per un livello di intestazione inferiore a questo
# ha ripristinato il conteggio per questo livello in modo che questo campo visualizzi "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # Il carattere separatore, che appare nel risultato del campo subito dopo il numero,
    # è un punto per impostazione predefinita. Se lasciamo questa proprietà nulla,
    # il nostro ultimo campo AUTONUMLGL visualizzerà "2.2.1." nel documento.
    self.assertIsNone(field.separator_character)
    # Impostare un carattere separatore personalizzato e rimuovere il punto finale
    # cambierà l'aspetto di quel campo da "2.2.1." a "2:2:1".
    # Applicheremo questo a tutti i campi che abbiamo creato.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # Questo testo appartiene al campo auto num legal sopra di esso.
    # Si chiuderà quando clicchiamo sulla freccia accanto al campo AUTONUMLGL corrispondente in Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

