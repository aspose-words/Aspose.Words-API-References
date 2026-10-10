---
title: FieldStyleRef.search_from_bottom property
linktitle: search_from_bottom property
articleTitle: search_from_bottom property
second_title: Aspose.Words for Python
description: "FieldStyleRef.search_from_bottom property. Gets or sets whether to search from the bottom of the current page, rather from the top."
type: docs
weight: 60
url: /tr/python-net/aspose.words.fields/fieldstyleref/search_from_bottom/
---

## FieldStyleRef.search_from_bottom property

Gets or sets whether to search from the bottom of the current page, rather from the top.


```python
@property
def search_from_bottom(self) -> bool:
    ...

@search_from_bottom.setter
def search_from_bottom(self, value: bool):
    ...

```

### Examples

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Microsoft Word liste şablonu kullanarak bir liste oluşturun.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Bu oluşturulan liste "1.a )" gösterecektir.
# Parantezden önceki boşluk, bastırabileceğimiz bir ayırıcı olmayan karakterdir.
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# Metin ekleyin ve STYLEREF alanlarının referans alacağı paragraf stillerini uygulayın.
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
# Üst bilgiye bir STYLEREF alanı yerleştirin ve belgede ilk "List Paragraph" stilindeki metni gösterin.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# Alt bilgiye bir STYLEREF alanı yerleştirin ve son metni göstermesini sağlayın.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# Ayrıca STYLEREF alanlarını listelerin numaralarına referans vermek için kullanabiliriz.
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

