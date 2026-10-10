---
title: PageSetup.border_surrounds_footer property
linktitle: border_surrounds_footer property
articleTitle: border_surrounds_footer property
second_title: Aspose.Words for Python
description: "PageSetup.border_surrounds_footer property. Specifies whether the page border includes or excludes the footer."
type: docs
weight: 50
url: /it/python-net/aspose.words/pagesetup/border_surrounds_footer/
---

## PageSetup.border_surrounds_footer property

Specifies whether the page border includes or excludes the footer.


```python
@property
def border_surrounds_footer(self) -> bool:
    ...

@border_surrounds_footer.setter
def border_surrounds_footer(self, value: bool):
    ...

```

### Remarks

Note, changing this property affects all sections in the document.


### Examples

Shows how to apply a border to the page and header/footer.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world! This is the main body text.')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer.')
builder.move_to_document_end()
# Inserisci un bordo a doppia linea blu.
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE
page_setup.borders.color = aspose.pydrawing.Color.blue
# L'oggetto PageSetup di una sezione ha i flag "BorderSurroundsHeader" e "BorderSurroundsFooter" che determinano
# se un bordo della pagina circonda il testo principale, includendo rispettivamente l'intestazione o il piè di pagina.
# Imposta il flag "BorderSurroundsHeader" su "true" per circondare l'intestazione con il nostro bordo,
# e poi imposta il flag "BorderSurroundsFooter" per lasciare il piè di pagina fuori dal bordo.
page_setup.border_surrounds_header = True
page_setup.border_surrounds_footer = False
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorder.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

