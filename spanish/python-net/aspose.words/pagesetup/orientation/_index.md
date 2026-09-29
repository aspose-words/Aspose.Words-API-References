---
title: PageSetup.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Python
description: "PageSetup.orientation property. Returns or sets the orientation of the page."
type: docs
weight: 290
url: /es/python-net/aspose.words/pagesetup/orientation/
---

## PageSetup.orientation property

Returns or sets the orientation of the page.


```python
@property
def orientation(self) -> aspose.words.Orientation:
    ...

@orientation.setter
def orientation(self, value: aspose.words.Orientation):
    ...

```

### Remarks

Changing [PageSetup.orientation](./) swaps [PageSetup.page_width](../page_width/) and [PageSetup.page_height](../page_height/).




### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifica las propiedades de configuración de página para la sección actual del constructor y agrega texto.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Si iniciamos una nueva sección usando un constructor de documentos,
# heredará las propiedades de configuración de página actuales del constructor.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.writeln('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageMargins.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

