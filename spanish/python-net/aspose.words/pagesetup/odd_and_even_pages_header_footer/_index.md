---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /es/python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
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
# Especifique que queremos encabezados y pies de página diferentes para la primera, las pares y las impares.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Cree los encabezados, luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
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
# A continuación se presentan dos tipos de encabezados/pies de página.
# 1 -  El encabezado/pie de página "Primary", que aparece en cada página de la sección.
# Podemos sobrescribir el encabezado/pie de página principal con un encabezado/pie de página de primera y de página par.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
# 2 -  El encabezado/pie de página "Even", que aparece en cada página par de esta sección.
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
# Cada sección tiene un objeto "PageSetup" que especifica propiedades relacionadas con la apariencia de la página
# como la orientación, el tamaño y los bordes.
# Establezca la propiedad "OddAndEvenPagesHeaderFooter" a "true"
# para mostrar el encabezado/pie de página par en las páginas pares.
# Establezca la propiedad "OddAndEvenPagesHeaderFooter" a "false"
# para mostrar el encabezado/pie de página principal en las páginas pares.
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.OddAndEvenPagesHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

