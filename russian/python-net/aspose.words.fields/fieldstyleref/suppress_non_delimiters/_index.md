---
title: FieldStyleRef.suppress_non_delimiters property
linktitle: suppress_non_delimiters property
articleTitle: suppress_non_delimiters property
second_title: Aspose.Words for Python
description: "FieldStyleRef.suppress_non_delimiters property. Gets or sets whether to suppress non-delimiter characters."
type: docs
weight: 80
url: /ru/python-net/aspose.words.fields/fieldstyleref/suppress_non_delimiters/
---

## FieldStyleRef.suppress_non_delimiters property

Gets or sets whether to suppress non-delimiter characters.


```python
@property
def suppress_non_delimiters(self) -> bool:
    ...

@suppress_non_delimiters.setter
def suppress_non_delimiters(self, value: bool):
    ...

```

### Examples

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте список, используя шаблон списка Microsoft Word.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Сгенерированный список будет отображать "1.a )".
# Пробел перед скобкой является неделимым символом, который мы можем подавить.
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# Добавьте текст и примените стили абзацев, на которые будут ссылаться поля STYLEREF.
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
# Разместите поле STYLEREF в заголовке и отобразите первый текст со стилем "List Paragraph" в документе.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# Разместите поле STYLEREF в нижнем колонтитуле и отобразите в нём последний текст.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# Мы также можем использовать поля STYLEREF для ссылки на номера списков.
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

