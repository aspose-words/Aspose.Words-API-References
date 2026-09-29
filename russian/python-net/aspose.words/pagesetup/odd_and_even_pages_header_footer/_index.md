---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /ru/python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
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
# Укажите, что нам нужны разные колонтитулы для первой, чётных и нечётных страниц.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Создайте колонтитулы, затем добавьте в документ три страницы, чтобы отобразить каждый тип колонтитула.
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
# Ниже представлены два типа заголовков/нижних колонтитулов.
# 1 -  "Primary" заголовок/нижний колонтитул, который отображается на каждой странице раздела.
# Мы можем переопределить основной заголовок/нижний колонтитул с помощью первого и четного заголовка/нижнего колонтитула.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
# 2 -  "Even" заголовок/нижний колонтитул, который отображается на каждой четной странице этого раздела.
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
# Каждый раздел имеет объект "PageSetup", который задает свойства, связанные с внешним видом страницы
# например, ориентацию, размер и границы.
# Установите свойство "OddAndEvenPagesHeaderFooter" в значение "true"
# чтобы отображать header/footer четных страниц на четных страницах.
# Установите свойство "OddAndEvenPagesHeaderFooter" в значение "false"
# чтобы отображать основной header/footer на четных страницах.
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.OddAndEvenPagesHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

