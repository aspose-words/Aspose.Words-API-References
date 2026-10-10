---
title: FieldToc.insert_hyperlinks property
linktitle: insert_hyperlinks property
articleTitle: insert_hyperlinks property
second_title: Aspose.Words for Python
description: "FieldToc.insert_hyperlinks property. Gets or sets whether to make the table of contents entries hyperlinks."
type: docs
weight: 100
url: /zh/python-net/aspose.words.fields/fieldtoc/insert_hyperlinks/
---

## FieldToc.insert_hyperlinks property

Gets or sets whether to make the table of contents entries hyperlinks.


```python
@property
def insert_hyperlinks(self) -> bool:
    ...

@insert_hyperlinks.setter
def insert_hyperlinks(self, value: bool):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# 插入一个目录（TOC）字段，它会将所有标题汇总到目录中。
# 对于每个标题，此字段将在左侧创建一行，文本使用该标题样式，
# 右侧显示标题所在的页码。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# 使用 BookmarkName 属性仅列出标题
# 仅列出位于名为 "MyBookmark" 的书签范围内的标题。
field.bookmark_name = 'MyBookmark'
# 带有内置标题样式（例如 "Heading 1"）的文本将被视为标题。
# 我们可以在此属性中指定其他样式，使其被目录识别为标题，并设定其目录层级。
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# 默认情况下，Styles/TOC 层级在 CustomStyles 属性中以逗号分隔，
# 但我们可以在此属性中设置自定义分隔符。
doc.field_options.custom_toc_style_separator = ';'
# 配置字段以排除任何目录层级超出此范围的标题。
field.heading_level_range = '1-3'
# 目录将不显示目录层级在此范围内的标题的页码。
field.page_number_omitting_level_range = '2-5'
# 设置自定义字符串，以分隔每个标题与其页码。
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
# 这两个标题的页码将被省略，因为它们位于 "2-5" 范围内。
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# 此条目不会出现，因为 "Heading 4" 超出了我们之前设置的 "1-3" 范围。
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# 此条目未显示，因为它位于目录指定的书签之外。
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

