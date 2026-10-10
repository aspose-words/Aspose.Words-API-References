---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /zh/python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
---

## PageSetup.odd_and_even_pages_header_footer property

True if the document has different headers and footers for odd-numbered and even-numbered pages.


```python
@property
def odd_and_even_pages_header_footer(self) -> bool:
    ...

@odd_and_even_pages_header_footer.setter
def odd_and_even_pages_header_footer(self, value: bool):
    ...

```

### Remarks

Note, changing this property affects all sections in the document.


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

Shows how to enable or disable even page headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 下面是两种页眉/页脚类型。
# 1 - "Primary" 页眉/页脚，出现在本节的每一页上。
# 我们可以通过首页和偶数页的页眉/页脚来覆盖主页眉/页脚。
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
# 2 - "Even" 页眉/页脚，出现在本节的每个偶数页上。
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.writeln('Even page header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_EVEN)
builder.writeln('Even page footer.')
builder.move_to_section(0)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# 每个章节都有一个 "PageSetup" 对象，指定页面外观相关属性
# 例如方向、尺寸和边框。
# 将 "OddAndEvenPagesHeaderFooter" 属性设置为 "true"
# 以在偶数页显示偶数页页眉/页脚。
# 将 "OddAndEvenPagesHeaderFooter" 属性设置为 "false"
# 以在偶数页显示主页眉/页脚。
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.OddAndEvenPagesHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

