---
title: FieldAutoNumLgl.remove_trailing_period property
linktitle: remove_trailing_period property
articleTitle: remove_trailing_period property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.remove_trailing_period property. Gets or sets whether to display the number without a trailing period."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldautonumlgl/remove_trailing_period/
---

## FieldAutoNumLgl.remove_trailing_period property

Gets or sets whether to display the number without a trailing period.


```python
@property
def remove_trailing_period(self) -> bool:
    ...

@remove_trailing_period.setter
def remove_trailing_period(self, value: bool):
    ...

```

### Examples

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# Los campos AUTONUMLGL muestran un número que se incrementa en cada campo AUTONUMLGL dentro de su nivel de encabezado actual.
# Estos campos mantienen un recuento separado para cada nivel de encabezado,
# y cada campo también muestra los recuentos de campos AUTONUMLGL para todos los niveles de encabezado por debajo del propio.
# Cambiar el recuento de cualquier nivel de encabezado restablece los recuentos de todos los niveles superiores a 1.
# Esto nos permite organizar nuestro documento en forma de lista de esquema.
# Este es el primer campo AUTONUMLGL en un nivel de encabezado 1, mostrando "1." en el documento.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# Este es el segundo campo AUTONUMLGL en un nivel de encabezado 1, por lo que mostrará "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# Este es el primer campo AUTONUMLGL en un nivel de encabezado 2,
# y el recuento AUTONUMLGL para el nivel de encabezado inferior es "2", por lo que mostrará "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# Este es el primer campo AUTONUMLGL en un nivel de encabezado 3.
# Funcionando de la misma manera que el campo anterior, mostrará "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# Este campo está en un nivel de encabezado 2, y su recuento AUTONUMLGL respectivo está en 2, por lo que el campo mostrará "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# Incrementar el recuento AUTONUMLGL para un nivel de encabezado inferior a este
# ha restablecido el recuento para este nivel de modo que este campo mostrará "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # El carácter separador, que aparece en el resultado del campo inmediatamente después del número,
    # es un punto por defecto. Si dejamos esta propiedad nula,
    # nuestro último campo AUTONUMLGL mostrará "2.2.1." en el documento.
    self.assertIsNone(field.separator_character)
    # Establecer un carácter separador personalizado y eliminar el punto final
    # cambiará la apariencia de ese campo de "2.2.1." a "2:2:1".
    # Aplicaremos esto a todos los campos que hemos creado.
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
    # Este texto pertenecerá al campo auto num legal que está encima.
    # Se colapsará cuando hagamos clic en la flecha junto al campo AUTONUMLGL correspondiente en Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

