---
title: FieldStyleRef.insert_paragraph_number_in_relative_context property
linktitle: insert_paragraph_number_in_relative_context property
articleTitle: insert_paragraph_number_in_relative_context property
second_title: Aspose.Words for Python
description: "FieldStyleRef.insert_paragraph_number_in_relative_context property. Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context."
type: docs
weight: 40
url: /sv/python-net/aspose.words.fields/fieldstyleref/insert_paragraph_number_in_relative_context/
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
# Skapa en lista baserad på en Microsoft Word-listmall.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Denna genererade lista kommer att visa \"1.a )\".
# Mellanslag före parentesen är ett icke-avgränsande tecken, som vi kan undertrycka.
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# Lägg till text och tillämpa styckeformat som STYLEREF-fält kommer att referera till.
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
# Placera ett STYLEREF-fält i sidhuvudet och visa den första \"List Paragraph\"-formaterade texten i dokumentet.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# Placera ett STYLEREF-fält i sidfoten och låt det visa den sista texten.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# Vi kan också använda STYLEREF-fält för att referera till listnumren i listor.
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

