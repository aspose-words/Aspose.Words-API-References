﻿---
title: FieldStyleRef.insert_paragraph_number_in_relative_context property
linktitle: insert_paragraph_number_in_relative_context property
articleTitle: insert_paragraph_number_in_relative_context property
second_title: Aspose.Words for Python
description: "FieldStyleRef.insert_paragraph_number_in_relative_context property. Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldstyleref/insert_paragraph_number_in_relative_context/
---

## FieldStyleRef.insert_paragraph_number_in_relative_context property

Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context.


```python
@property
def insert_paragraph_number_in_relative_context(self) -> bool:
    ...

@insert_paragraph_number_in_relative_context.setter
def insert_paragraph_number_in_relative_context(self, value: bool):
    ...

```

### Examples

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create a list based using a Microsoft Word list template.
list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# This generated list will display "1.a )".
# Space before the bracket is a non-delimiter character, which we can suppress.
list.list_levels[0].number_format = '\x00.'
list.list_levels[1].number_format = '\x01 )'
# Add text and apply paragraph styles that STYLEREF fields will reference.
builder.list_format.list = list
builder.list_format.list_indent()
builder.paragraph_format.style = doc.styles.get_by_name('List Paragraph')
builder.writeln('Item 1')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln('Item 2')
builder.paragraph_format.style = doc.styles.get_by_name('List Paragraph')
builder.writeln('Item 3')
builder.list_format.remove_numbers()
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Place a STYLEREF field in the header and display the first "List Paragraph"-styled text in the document.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# Place a STYLEREF field in the footer, and have it display the last text.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# We can also use STYLEREF fields to reference the list numbers of lists.
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

