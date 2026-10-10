---
title: HeaderFooter.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "HeaderFooter.parent_section property. Gets the parent section of this story."
type: docs
weight: 60
url: /es/python-net/aspose.words/headerfooter/parent_section/
---

## HeaderFooter.parent_section property

Gets the parent section of this story.


```python
@property
def parent_section(self) -> aspose.words.Section:
    ...

```

### Remarks

[HeaderFooter.parent_section](./) is equivalent to [Node.parent_node](../../node/parent_node/) casted to [Section](../../section/).




### Examples

Shows how to link headers and footers between sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
# Desplácese a la primera sección y cree un encabezado y un pie de página. Por defecto,
# el encabezado y el pie de página solo aparecerán en las páginas de la sección que los contiene.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Podemos vincular los encabezados/pies de página de una sección a los encabezados/pies de página de la sección anterior
# para permitir que la sección vinculada muestre los encabezados/pies de la sección enlazada.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Cada sección seguirá teniendo sus propios objetos de encabezado/pie de página. Cuando vinculamos secciones,
# la sección vinculante mostrará los encabezados/pies de la sección enlazada mientras conserva los suyos propios.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Vincule los encabezados/pies de la tercera sección a los encabezados/pies de la segunda sección.
# La segunda sección ya está vinculada a los encabezados/pies de la primera sección,
# por lo que vincular a la segunda sección creará una cadena de enlaces.
# La primera, segunda y ahora la tercera sección mostrarán todos los encabezados de la primera sección.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Podemos desvincular los encabezados/pies de una sección anterior pasando "false" al llamar al método LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# También podemos seleccionar solo un tipo específico de encabezado/pie de página para vincular usando este método.
# La tercera sección ahora tendrá el mismo pie de página que la segunda y la primera secciones, pero no el encabezado.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Los encabezados/pies de la primera sección no pueden enlazarse a nada porque no hay una sección anterior.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Todos los encabezados/pies de la segunda sección están enlazados a los encabezados/pies de la primera sección.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# En la tercera sección, solo el pie está enlazado al pie de la primera sección a través de la segunda sección.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

