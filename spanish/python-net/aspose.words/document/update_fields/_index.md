---
title: Document.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Document.update_fields method. Updates the values of fields in the whole document."
type: docs
weight: 800
url: /es/python-net/aspose.words/document/update_fields/
---

## update_fields() {#default}

Updates the values of fields in the whole document.


```python
def update_fields(self):
    ...
```

### Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.update_page_layout()](../update_page_layout/#default).

Use the [Document.normalize_field_types()](../normalize_field_types/#default) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.update_fields()](../../range/update_fields/#default).




### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte una tabla de contenido para la primera página del documento.
# Configure la tabla para que incluya párrafos con encabezados de niveles del 1 al 3.
# Además, configure sus entradas para que sean hipervínculos que nos lleven
# a la ubicación del encabezado al hacer clic izquierdo en Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Llena la tabla de contenido añadiendo párrafos con estilos de encabezado.
# Cada encabezado de este tipo con un nivel entre 1 y 3 creará una entrada en la tabla.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Una tabla de contenido es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un campo QUOTE, que mostrará el valor de su propiedad Text.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# Inserte un campo QUOTE y anide un campo DATE dentro de él.
# Los campos DATE actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
# Anidar el campo DATE dentro del campo QUOTE de esta manera congelará su valor
# a la fecha en que creamos el documento.
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# Actualice todos los campos para que muestren sus resultados correctos.
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un objeto UserInformation y configúrelo como la fuente de datos para los campos que muestran información del usuario.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Inserte los campos USERNAME, USERINITIALS y USERADDRESS, que muestran valores de
# las respectivas propiedades del objeto UserInformation que hemos creado arriba.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# El objeto de opciones de campo también tiene un usuario predeterminado estático al que los campos de todos los documentos pueden referirse.
aw.fields.UserInformation.default_user.name = 'Default User'
aw.fields.UserInformation.default_user.initials = 'D. U.'
aw.fields.UserInformation.default_user.address = 'One Microsoft Way'
doc.field_options.current_user = aw.fields.UserInformation.default_user
self.assertEqual('Default User', builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual('D. U.', builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual('One Microsoft Way', builder.insert_field(field_code=' USERADDRESS ').result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.CurrentUser.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

