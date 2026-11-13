---
title: PageSetup.multiple_pages property
linktitle: multiple_pages property
articleTitle: multiple_pages property
second_title: Aspose.Words for Python
description: "PageSetup.multiple_pages property. For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet."
type: docs
weight: 270
url: /es/python-net/aspose.words/pagesetup/multiple_pages/
---

## PageSetup.multiple_pages property

For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet.


```python
@property
def multiple_pages(self) -> aspose.words.settings.MultiplePagesType:
    ...

@multiple_pages.setter
def multiple_pages(self, value: aspose.words.settings.MultiplePagesType):
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

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# Inserte texto que abarque 16 páginas.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de pliegue de libro.
# Cuando imprimimos este documento a doble cara, podemos tomar las páginas para apilarlas
# y doblarlas todas por la mitad de una vez. El contenido del documento se alineará en un pliegue de libro.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Solo podemos especificar el número de hojas en múltiplos de 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

