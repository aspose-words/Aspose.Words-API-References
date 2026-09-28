---
title: PageSetup.border_surrounds_footer property
linktitle: border_surrounds_footer property
articleTitle: border_surrounds_footer property
second_title: Aspose.Words for Python
description: "PageSetup.border_surrounds_footer property. Specifies whether the page border includes or excludes the footer."
type: docs
weight: 50
url: /de/python-net/aspose.words/pagesetup/border_surrounds_footer/
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
# Fügen Sie einen blauen Doppel-Linien-Rahmen ein.
page_setup = doc.sections[0].page_setup
page_setup.borders.line_style = aw.LineStyle.DOUBLE
page_setup.borders.color = aspose.pydrawing.Color.blue
# Ein PageSetup-Objekt eines Abschnitts hat die Flags "BorderSurroundsHeader" und "BorderSurroundsFooter", die bestimmen
# ob ein Seitenrahmen den Haupttext umschließt, bzw. den Header oder Footer einschließt.
# Setzen Sie das Flag "BorderSurroundsHeader" auf "true", um den Header mit unserem Rahmen zu umschließen,
# und setzen Sie anschließend das Flag "BorderSurroundsFooter", um den Footer außerhalb des Rahmens zu lassen.
page_setup.border_surrounds_header = True
page_setup.border_surrounds_footer = False
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorder.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

