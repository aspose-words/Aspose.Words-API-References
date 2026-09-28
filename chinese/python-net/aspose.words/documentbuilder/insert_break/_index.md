---
title: DocumentBuilder.insert_break method
linktitle: insert_break method
articleTitle: insert_break method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_break method. Inserts a break of the specified type into the document."
type: docs
weight: 260
url: /zh/python-net/aspose.words/documentbuilder/insert_break/
---

## insert_break(break_type) {#breaktype}

Inserts a break of the specified type into the document.


```python
def insert_break(self, break_type: aspose.words.BreakType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| break_type | [BreakType](../../breaktype/) | Specifies the type of the break to insert. |

### Remarks

Use this method to insert paragraph, page, column, section or line break into the document.


### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 指定我们希望为首页、偶数页和奇数页设置不同的页眉和页脚。
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# 创建页眉，然后向文档添加三页以显示每种页眉类型。
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 为文档的首页插入目录。
# 配置目录以捕获级别 1 到 3 的标题段落。
# 此外，将其条目设置为超链接，使我们能够
# 在 Microsoft Word 中左键单击标题时跳转到标题位置。
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 通过添加带有标题样式的段落来填充目录。
# 每个级别在 1 到 3 之间的此类标题都会在目录中创建一个条目。
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
# 目录是需要更新以显示最新结果的字段类型。
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 修改构建器当前节的页面设置属性并添加文本。
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# 如果我们使用文档构建器开始一个新节，
# 它将继承构建器当前的页面设置属性。
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# 我们可以使用 "ClearFormatting" 方法将其页面设置属性恢复为默认值。
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

