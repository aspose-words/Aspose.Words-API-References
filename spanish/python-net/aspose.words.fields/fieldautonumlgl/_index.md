---
title: FieldAutoNumLgl class
linktitle: FieldAutoNumLgl class
articleTitle: FieldAutoNumLgl class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldAutoNumLgl class. Implements the AUTONUMLGL field"
type: docs
weight: 130
url: /es/python-net/aspose.words.fields/fieldautonumlgl/
---

## FieldAutoNumLgl class

Implements the AUTONUMLGL field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts an automatic number in legal format.


**Inheritance:** [FieldAutoNumLgl](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAutoNumLgl()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [remove_trailing_period](./remove_trailing_period/) | Gets or sets whether to display the number without a trailing period. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [separator_character](./separator_character/) | Gets or sets the separator character to be used. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

