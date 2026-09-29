---
title: FieldStyleRef.insert_paragraph_number property
linktitle: insert_paragraph_number property
articleTitle: insert_paragraph_number property
second_title: Aspose.Words for Python
description: "FieldStyleRef.insert_paragraph_number property. Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldstyleref/insert_paragraph_number/
---

## FieldStyleRef.insert_paragraph_number property

Gets or sets whether to insert the paragraph number of the referenced paragraph exactly as it appears in the document.


```python
@property
def insert_paragraph_number(self) -> bool:
    ...

@insert_paragraph_number.setter
def insert_paragraph_number(self, value: bool):
    ...

```

### Examples

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree una lista basada en una plantilla de lista de Microsoft Word.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Esta lista generada mostrará "1.a )".
# El espacio antes del corchete es un carácter no delimitador, que podemos suprimir.
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# Agregue texto y aplique estilos de párrafo que los campos STYLEREF referenciarán.
builder.list_format.list = doc_list
builder.list_format.list_indent()
builder.paragraph_format.style = doc.styles.get_by_name('List Paragraph')
builder.writeln('Item 1')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln('Item 2')
builder.paragraph_format.style = doc.styles.get_by_name('List Paragraph')
builder.writeln('Item 3')
builder.list_format.remove_numbers()
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Coloque un campo STYLEREF en el encabezado y muestre el primer texto con estilo "List Paragraph" del documento.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# Coloque un campo STYLEREF en el pie de página y haga que muestre el último texto.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# También podemos usar campos STYLEREF para referenciar los números de lista de las listas.
builder.write('\nParagraph number: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'Quote'
field.insert_paragraph_number = True
builder.write('\nParagraph number, relative context: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'Quote'
field.insert_paragraph_number_in_relative_context = True
builder.write('\nParagraph number, full context: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'Quote'
field.insert_paragraph_number_in_full_context = True
builder.write('\nParagraph number, full context, non-delimiter chars suppressed: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'Quote'
field.insert_paragraph_number_in_full_context = True
field.suppress_non_delimiters = True
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.STYLEREF.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldStyleRef](../)

