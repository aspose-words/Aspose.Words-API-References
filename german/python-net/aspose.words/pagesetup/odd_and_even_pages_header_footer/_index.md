---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /de/python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
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
# Geben Sie an, dass wir unterschiedliche Kopf- und Fußzeilen für die erste, gerade und ungerade Seiten wünschen.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Erstellen Sie die Kopfzeilen und fügen Sie dann dem Dokument drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
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
# Unten sind zwei Arten von Headern/Footern aufgeführt.
# 1 -  Der "Primary"-Header/Footer, der auf jeder Seite des Abschnitts erscheint.
# Wir können den primären Header/Footer durch einen ersten und einen geraden Seiten-Header/Footer überschreiben.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
# 2 -  Der "Even"-Header/Footer, der auf jeder geraden Seite dieses Abschnitts erscheint.
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
# Jeder Abschnitt hat ein "PageSetup"-Objekt, das seitenspezifische Eigenschaften festlegt
# wie Ausrichtung, Größe und Ränder.
# Setzen Sie die "OddAndEvenPagesHeaderFooter"-Eigenschaft auf "true"
# um die Kopf-/Fußzeile für gerade Seiten auf geraden Seiten anzuzeigen.
# Setzen Sie die "OddAndEvenPagesHeaderFooter"-Eigenschaft auf "false"
# um die primäre Kopf-/Fußzeile auf geraden Seiten anzuzeigen.
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.OddAndEvenPagesHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

