---
title: FieldToc.page_number_omitting_level_range property
linktitle: page_number_omitting_level_range property
articleTitle: page_number_omitting_level_range property
second_title: Aspose.Words for Python
description: "FieldToc.page_number_omitting_level_range property. Gets or sets a range of levels of the table of contents entries from which to omits page numbers."
type: docs
weight: 110
url: /es/python-net/aspose.words.fields/fieldtoc/page_number_omitting_level_range/
---

## FieldToc.page_number_omitting_level_range property

Gets or sets a range of levels of the table of contents entries from which to omits page numbers.


```python
@property
def page_number_omitting_level_range(self) -> str:
    ...

@page_number_omitting_level_range.setter
def page_number_omitting_level_range(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# Inserte un campo TOC, que compilará todos los encabezados en una tabla de contenido.
# Para cada encabezado, este campo creará una línea con el texto en ese estilo de encabezado a la izquierda,
# y la página donde aparece el encabezado a la derecha.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Utilice la propiedad BookmarkName para listar solo los encabezados
# que aparecen dentro de los límites de un marcador con el nombre "MyBookmark".
field.bookmark_name = 'MyBookmark'
# El texto con un estilo de encabezado incorporado, como "Heading 1", aplicado a él contará como un encabezado.
# Podemos nombrar estilos adicionales para que la TOC los reconozca como encabezados en esta propiedad y sus niveles TOC.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# Por defecto, los niveles Styles/TOC se separan en la propiedad CustomStyles por una coma,
# pero podemos establecer un delimitador personalizado en esta propiedad.
doc.field_options.custom_toc_style_separator = ';'
# Configure el campo para excluir cualquier encabezado que tenga niveles TOC fuera de este rango.
field.heading_level_range = '1-3'
# La TOC no mostrará los números de página de los encabezados cuyos niveles TOC estén dentro de este rango.
field.page_number_omitting_level_range = '2-5'
# Establezca una cadena personalizada que separe cada encabezado de su número de página.
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# Estos dos encabezados tendrán los números de página omitidos porque están dentro del rango "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Esta entrada no aparece porque "Heading 4" está fuera del rango "1-3" que establecimos anteriormente.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Esta entrada no aparece porque está fuera del marcador especificado por la tabla de contenido.
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

