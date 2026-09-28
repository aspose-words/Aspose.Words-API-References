---
title: PageSetup.page_starting_number property
linktitle: page_starting_number property
articleTitle: page_starting_number property
second_title: Aspose.Words for Python
description: "PageSetup.page_starting_number property. Gets or sets the starting page number of the section."
type: docs
weight: 330
url: /zh/python-net/aspose.words/pagesetup/page_starting_number/
---

## PageSetup.page_starting_number property

Gets or sets the starting page number of the section.


```python
@property
def page_starting_number(self) -> int:
    ...

@page_starting_number.setter
def page_starting_number(self, value: int):
    ...

```

### Remarks

The [PageSetup.restart_page_numbering](../restart_page_numbering/) property, if set to ``False``, will override the
[PageSetup.page_starting_number](./) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# 将文档构建器移动到第一节的主页眉，
# 该节的每一页都会显示它。
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# 插入一个 PAGE 域，它将显示当前页的页码。
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# 配置该节，使 PAGE 域显示的页码从 5 开始。
# 另外，配置所有 PAGE 域使用大写罗马数字显示页码。
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# 为第二节创建另一个主页眉，并包含另一个 PAGE 域。
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# 配置该节，使 PAGE 域显示的页码从 10 开始。
# 另外，配置所有 PAGE 域使用阿拉伯数字显示页码。
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

