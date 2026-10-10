---
title: PageSetup.different_first_page_header_footer property
linktitle: different_first_page_header_footer property
articleTitle: different_first_page_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.different_first_page_header_footer property. True if a different header or footer is used on the first page."
type: docs
weight: 110
url: /sv/python-net/aspose.words/pagesetup/different_first_page_header_footer/
---

## PageSetup.different_first_page_header_footer property

True if a different header or footer is used on the first page.


```python
@property
def different_first_page_header_footer(self) -> bool:
    ...

@different_first_page_header_footer.setter
def different_first_page_header_footer(self, value: bool):
    ...

```

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ange att vi vill ha olika sidhuvuden och sidfötter för första, jämna och udda sidor.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Skapa sidhuvudena, lägg sedan till tre sidor i dokumentet för att visa varje sidhuvudstyp.
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

Shows how to track the order in which a text replacement operation traverses nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
first_page_section = doc.first_section
logger = self.ReplaceLog()
options = aw.replacing.FindReplaceOptions(replacing_callback=logger)
# Att använda ett annat sidhuvud/sidfötter för den första sidan kommer att påverka sökordningen.
first_page_section.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.range.replace_regex(pattern='(header|footer)', replacement='', options=options)
if different_first_page_header_footer:
    self.assertEqual('First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n', logger.text.replace('\r', ''))
else:
    self.assertEqual('Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n', logger.text.replace('\r', ''))
```

Shows how to track the order in which a text replacement operation traverses nodes (ReplaceLog).

```python
class ReplaceLog(aw.replacing.IReplacingCallback):

    @property
    def text(self):
        return str.join('', self.m_text_builder)

    def __init__(self):
        self.m_text_builder = []

    def replacing(self, args):
        self.m_text_builder.append(args.match_node.get_text() + '\n')
        return aw.replacing.ReplaceAction.SKIP
```

Shows how to enable or disable primary headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Nedan finns två typer av sidhuvuden/sidfötter.
# 1 -  Det "First"-sidhuvud/sidfot, som visas på den första sidan i sektionen.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.writeln('First page header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_FIRST)
builder.writeln('First page footer.')
# 2 -  Det "Primary"-sidhuvud/sidfot, som visas på varje sida i sektionen.
# Vi kan åsidosätta det primära sidhuvudet/sidfoten med ett första och ett jämnt sidhuvud/sidfot.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
builder.move_to_section(0)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Varje sektion har ett "PageSetup"-objekt som specificerar sidutseende-relaterade egenskaper
# såsom orientering, storlek och kanter.
# Ställ in egenskapen "DifferentFirstPageHeaderFooter" till "true" för att tillämpa det första sidhuvudet/sidfoten på den första sidan.
# Ställ in egenskapen "DifferentFirstPageHeaderFooter" till "false"
# för att få den första sidan att visa det primära sidhuvudet/sidfoten.
builder.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.DifferentFirstPageHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

