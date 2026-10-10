---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /es/python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```python
@property
def rtl_gutter(self) -> bool:
    ...

@rtl_gutter.setter
def rtl_gutter(self, value: bool):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Inserta texto que abarque varias páginas.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Un canal agrega espacios en blanco al margen izquierdo o derecho de la página,
# lo que compensa el pliegue central de las páginas de un libro que invade el diseño de la página.
page_setup = doc.sections[0].page_setup
# Determina cuánto espacio tienen nuestras páginas para texto dentro de los márgenes y luego agrega una cantidad para acolchar un margen.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Establece la propiedad "RtlGutter" en "true" para colocar el gutter en una posición más adecuada para texto de derecha a izquierda.
page_setup.rtl_gutter = True
# Establece la propiedad "MultiplePages" en "MultiplePagesType.MirrorMargins" para alternar
# la posición del lado izquierdo/derecho de los márgenes en cada página.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

