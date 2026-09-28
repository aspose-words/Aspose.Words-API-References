---
title: FieldStyleRef.insert_paragraph_number_in_full_context property
linktitle: insert_paragraph_number_in_full_context property
articleTitle: insert_paragraph_number_in_full_context property
second_title: Aspose.Words for Python
description: "FieldStyleRef.insert_paragraph_number_in_full_context property. Gets or sets whether to insert the paragraph number of the referenced paragraph in full context."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldstyleref/insert_paragraph_number_in_full_context/
---

## FieldStyleRef.insert_paragraph_number_in_full_context property

Gets or sets whether to insert the paragraph number of the referenced paragraph in full context.


```python
@property
def insert_paragraph_number_in_full_context(self) -> bool:
    ...

@insert_paragraph_number_in_full_context.setter
def insert_paragraph_number_in_full_context(self, value: bool):
    ...

```

### Examples

Shows how to use STYLEREF fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用 Microsoft Word 列表模板创建基于列表的列表。
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# 生成的列表将显示 "1.a )"。
# 括号前的空格是非分隔符字符，我们可以将其抑制。
doc_list.list_levels[0].number_format = '\x00.'
doc_list.list_levels[1].number_format = '\x01 )'
# 添加文本并应用段落样式，STYLEREF 字段将引用这些样式。
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
# 在页眉中放置一个 STYLEREF 字段，显示文档中第一个 "List Paragraph" 样式的文本。
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
# 在页脚中放置一个 STYLEREF 字段，并让它显示最后的文本。
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_STYLE_REF, update_field=True).as_field_style_ref()
field.style_name = 'List Paragraph'
field.search_from_bottom = True
builder.move_to_document_end()
# 我们还可以使用 STYLEREF 字段引用列表的编号。
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

