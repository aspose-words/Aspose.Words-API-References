---
title: PageSetup.paper_size property
linktitle: paper_size property
articleTitle: paper_size property
second_title: Aspose.Words for Python
description: "PageSetup.paper_size property. Returns or sets the paper size."
type: docs
weight: 350
url: /es/python-net/aspose.words/pagesetup/paper_size/
---

## PageSetup.paper_size property

Returns or sets the paper size.


```python
@property
def paper_size(self) -> aspose.words.PaperSize:
    ...

@paper_size.setter
def paper_size(self, value: aspose.words.PaperSize):
    ...

```

### Remarks

Setting this property updates [PageSetup.page_width](../page_width/) and [PageSetup.page_height](../page_height/) values.
Setting this value to [PaperSize.CUSTOM](../../papersize/#CUSTOM) does not change existing values.




### Examples

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

Shows how to set page sizes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Podemos cambiar el tamaño de la página actual a un tamaño predefinido
# usando la propiedad "PaperSize" del objeto PageSetup de esta sección.
builder.page_setup.paper_size = aw.PaperSize.TABLOID
self.assertEqual(792, builder.page_setup.page_width)
self.assertEqual(1224, builder.page_setup.page_height)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
# Cada sección tiene su propio objeto PageSetup. Cuando usamos un document builder para crear una nueva sección,
# el objeto PageSetup de esa sección hereda todos los valores del objeto PageSetup de la sección anterior.
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
self.assertEqual(aw.PaperSize.TABLOID, builder.page_setup.paper_size)
builder.page_setup.paper_size = aw.PaperSize.A5
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
self.assertEqual(419.55, builder.page_setup.page_width)
self.assertEqual(595.3, builder.page_setup.page_height)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
# Establece un tamaño personalizado para las páginas de esta sección.
builder.page_setup.page_width = 620
builder.page_setup.page_height = 480
self.assertEqual(aw.PaperSize.CUSTOM, builder.page_setup.paper_size)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PaperSizes.docx')
```

Shows how to set the paper size of JisB4 or JisB5.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
page_setup = doc.first_section.page_setup
# Establezca el tamaño del papel a JisB4 (257x364mm).
page_setup.paper_size = aw.PaperSize.JIS_B4
# Alternativamente, establezca el tamaño del papel a JisB5. (182x257mm).
page_setup.paper_size = aw.PaperSize.JIS_B5
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Un documento en blanco contiene una sección, un cuerpo y un párrafo.
# Llame al método "RemoveAllChildren" para eliminar todos esos nodos,
# y terminará con un nodo de documento sin hijos.
doc.remove_all_children()
# Este documento ahora no tiene nodos hijos compuestos a los que podamos añadir contenido.
# Si deseamos editarlo, necesitaremos volver a poblar su colección de nodos.
# Primero, cree una nueva sección y luego añádala como hijo al nodo raíz del documento.
section = aw.Section(doc)
doc.append_child(section)
# Establezca algunas propiedades de configuración de página para la sección.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Una sección necesita un cuerpo, que contendrá y mostrará todo su contenido
# en la página entre el encabezado y el pie de página de la sección.
body = aw.Body(doc)
section.append_child(body)
# Cree un párrafo, establezca algunas propiedades de formato y luego añádalo como hijo al cuerpo.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Finalmente, añada contenido al documento. Cree un run,
# establezca su apariencia y contenido, y luego añádalo como hijo al párrafo.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

