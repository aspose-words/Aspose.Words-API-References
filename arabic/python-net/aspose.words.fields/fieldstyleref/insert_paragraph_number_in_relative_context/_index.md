---
title: FieldStyleRef.insert_paragraph_number_in_relative_context property
linktitle: insert_paragraph_number_in_relative_context property
articleTitle: insert_paragraph_number_in_relative_context property
second_title: Aspose.Words for Python
description: "FieldStyleRef.insert_paragraph_number_in_relative_context property. Gets or sets whether to insert the paragraph number of the referenced paragraph in relative context."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldstyleref/insert_paragraph_number_in_relative_context/
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
# أنشئ قائمة مستندة إلى قالب قائمة من Microsoft Word.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# ستعرض هذه القائمة المُولدة "1.a )".
# المسافة قبل القوس هي حرف غير فاصل، يمكننا كتمها.
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# أضف نصًا وطبق أنماط الفقرات التي ستشير إليها حقول STYLEREF.
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
# ضع حقل STYLEREF في الترويسة وعرض النص الأول المنسق بنمط "List Paragraph" في المستند.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# ضع حقل STYLEREF في التذييل، واجعله يعرض النص الأخير.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# يمكننا أيضًا استخدام حقول STYLEREF للإشارة إلى أرقام القوائم.
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

