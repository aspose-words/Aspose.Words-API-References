---
title: FieldToc.hide_in_web_layout property
linktitle: hide_in_web_layout property
articleTitle: hide_in_web_layout property
second_title: Aspose.Words for Python
description: "FieldToc.hide_in_web_layout property. Gets or sets whether to hide tab leader and page numbers in Web layout view."
type: docs
weight: 90
url: /ru/python-net/aspose.words.fields/fieldtoc/hide_in_web_layout/
---

## FieldToc.hide_in_web_layout property

Gets or sets whether to hide tab leader and page numbers in Web layout view.


```python
@property
def hide_in_web_layout(self) -> bool:
    ...

@hide_in_web_layout.setter
def hide_in_web_layout(self, value: bool):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# Вставьте поле Оглавления (TOC), которое соберёт все заголовки в таблицу содержимого.
# Для каждого заголовка это поле создаст строку с текстом в стиле этого заголовка слева,
# а номер страницы, на которой находится заголовок, — справа.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Используйте свойство BookmarkName, чтобы перечислять только заголовки
# которые находятся в пределах закладки с именем "MyBookmark".
field.bookmark_name = 'MyBookmark'
# Текст с встроенным стилем заголовка, например "Heading 1", применённый к нему, будет считаться заголовком.
# Мы можем указать дополнительные стили, которые будут распознаны как заголовки Оглавлением (TOC) в этом свойстве, и их уровни Оглавления.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# По умолчанию стили/уровни Оглавления разделяются в свойстве CustomStyles запятой,
# но мы можем задать пользовательский разделитель в этом свойстве.
doc.field_options.custom_toc_style_separator = ';'
# Настройте поле, чтобы исключить любые заголовки, у которых уровни Оглавления находятся за пределами этого диапазона.
field.heading_level_range = '1-3'
# Оглавление не будет отображать номера страниц заголовков, уровни Оглавления которых находятся в этом диапазоне.
field.page_number_omitting_level_range = '2-5'
# Установите пользовательскую строку, которая будет разделять каждый заголовок и его номер страницы.
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
# Эти два заголовка будут без номеров страниц, потому что они находятся в диапазоне "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# Эта запись не отображается, потому что "Heading 4" находится за пределами диапазона "1-3", установленного ранее.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# Эта запись не отображается, потому что она находится за пределами закладки, указанной в оглавлении.
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

