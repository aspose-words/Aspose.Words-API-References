---
title: Run constructor
linktitle: Run constructor
articleTitle: Run constructor
second_title: Aspose.Words for Python
description: "aspose.words.Run constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words/run/__init__/
---

## Run(doc) {#documentbase}

Initializes a new instance of the [Run](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Run](../) to the document use [CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
on the paragraph where you want the run inserted.




## Run(doc, text) {#documentbase_str}

Initializes a new instance of the **Run** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| text | str | The text of the run. |

### Remarks

When [Run](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Run](../) to the document use [CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
on the paragraph where you want the run inserted.




## Examples

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

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc=doc, text='Hello world!')
font = run.font
font.name = 'Courier New'
font.size = 36
font.highlight_color = aspose.pydrawing.Color.yellow
doc.first_section.body.first_paragraph.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.CreateFormattedRun.docx')
```

## See Also

* module [aspose.words](../../)
* class [Run](../)

