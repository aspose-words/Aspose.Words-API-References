---
title: Paragraph.paragraph_format property
linktitle: paragraph_format property
articleTitle: paragraph_format property
second_title: Aspose.Words for Python
description: "Paragraph.paragraph_format property. Provides access to the paragraph formatting properties."
type: docs
weight: 190
url: /es/python-net/aspose.words/paragraph/paragraph_format/
---

## Paragraph.paragraph_format property

Provides access to the paragraph formatting properties.


```python
@property
def paragraph_format(self) -> aspose.words.ParagraphFormat:
    ...

```

### Examples

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
* class [Paragraph](../)

