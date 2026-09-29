---
title: FieldToa class
linktitle: FieldToa class
articleTitle: FieldToa class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldToa class. Implements the TOA field"
type: docs
weight: 1060
url: /es/python-net/aspose.words.fields/fieldtoa/
---

## FieldToa class

Implements the TOA field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds a table of authorities (that is, a list of the references in a legal document, such as references
to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the
entries specified by TA fields.


**Inheritance:** [FieldToa](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldToa()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the table. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_category](./entry_category/) | Gets or sets the integral category for entries included in the table. |
| [entry_separator](./entry_separator/) | Gets or sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [page_number_list_separator](./page_number_list_separator/) | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [page_range_separator](./page_range_separator/) | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [remove_entry_formatting](./remove_entry_formatting/) | Gets or sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_name](./sequence_name/) | Gets or sets the name of a sequence whose number is included with the page number. |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_heading](./use_heading/) | Gets or sets whether to include the category heading for the entries in a table of authorities. |
| [use_passim](./use_passim/) | Gets or sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

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

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un campo TOA, que creará una entrada para cada campo TA en el documento,
# mostrando citas largas y números de página para cada entrada.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Establezca la categoría de entrada para nuestra tabla. Este TOA ahora solo incluirá campos TA
# que tengan un valor coincidente en su propiedad EntryCategory.
field_toa.entry_category = '1'
# Además, la categoría de Tabla de Autoridades en el índice 1 es "Cases",
# que aparecerá como el título de nuestra tabla si establecemos esta variable en verdadero.
field_toa.use_heading = True
# Podemos filtrar aún más los campos TA nombrando un marcador del que deberán estar dentro de los límites del TOA.
field_toa.bookmark_name = 'MyBookmark'
# Por defecto, una pestaña de línea punteada que abarca toda la página aparece entre la cita del campo TA
# y su número de página. Podemos reemplazarla con cualquier texto que pongamos en esta propiedad.
# Insertar un carácter de tabulación preservará la tabulación original.
field_toa.entry_separator = ' \t p.'
# Si tenemos múltiples entradas TA que comparten la misma cita larga,
# todos sus respectivos números de página aparecerán en una sola fila.
# Podemos usar esta propiedad para especificar una cadena que separará sus números de página.
field_toa.page_number_list_separator = ' & p. '
# Podemos establecer esto en true para que nuestra tabla muestre la palabra "passim"
# si hay cinco o más números de página en una fila.
field_toa.use_passim = True
# Un campo TA puede referirse a un rango de páginas.
# Podemos especificar una cadena aquí para que aparezca entre los números de página inicial y final de dichos rangos.
field_toa.page_range_separator = ' to '
# El formato de los campos TA se transferirá a nuestra tabla.
# Podemos desactivar esto configurando la bandera RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Este campo TA no aparecerá como una entrada en la TOA ya que está fuera
# de los límites del marcador que especifica la propiedad BookmarkName de la TOA.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Este campo TA está dentro del marcador,
# pero la categoría de la entrada no coincide con la de la tabla, por lo que el campo TA no la incluirá.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Esta entrada aparecerá en la tabla.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Una tabla TOA no muestra citas cortas,
# pero podemos usarlas como abreviatura para referirnos a nombres de fuentes extensos que varios campos TA referencian.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Podemos formatear el número de página para hacerlo negrita/cursiva usando las siguientes propiedades.
# Seguiremos viendo estos efectos si configuramos nuestra tabla para ignorar el formato.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Podemos configurar los campos TA para que sus entradas TOA se refieran a un rango de páginas que abarca un marcador.
# Observe que esta entrada se refiere a la misma fuente que la anterior para compartir una fila en nuestra tabla.
# Esta fila tendrá el número de página de la entrada anterior y el rango de páginas de esta entrada,
# con la lista de páginas de la tabla y los separadores de rango de números de página entre los números de página.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Si hemos habilitado la función "Passim" de nuestra tabla, tener 5 o más entradas TA con la misma fuente la activará.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

