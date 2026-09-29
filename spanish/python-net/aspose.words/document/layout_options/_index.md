---
title: Document.layout_options property
linktitle: layout_options property
articleTitle: layout_options property
second_title: Aspose.Words for Python
description: "Document.layout_options property. Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document."
type: docs
weight: 260
url: /es/python-net/aspose.words/document/layout_options/
---

## Document.layout_options property

Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document.



```python
@property
def layout_options(self) -> aspose.words.layout.LayoutOptions:
    ...

```

### Examples

Shows how to hide text in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserta texto oculto, luego especifica si deseamos omitirlo de un documento renderizado.
builder.writeln('This text is not hidden.')
builder.font.hidden = True
builder.writeln('This text is hidden.')
doc.layout_options.show_hidden_text = show_hidden_text
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsHiddenText.pdf')
```

Shows how to show paragraph marks in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agrega algunos párrafos, luego habilita los símbolos de fin de párrafo para mostrar los finales de los párrafos
# con el símbolo de párrafo (¶) cuando renderizamos el documento.
builder.writeln('Hello world!')
builder.writeln('Hello again!')
doc.layout_options.show_paragraph_marks = show_paragraph_marks
doc.save(file_name=ARTIFACTS_DIR + 'Document.LayoutOptionsParagraphMarks.pdf')
```

Shows how to alter the appearance of revisions in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserta una revisión, luego cambia el color de todas las revisiones a verde.
builder.writeln('This is not a revision.')
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('This is a revision.')
doc.stop_track_revisions()
builder.writeln('This is not a revision.')
# Elimina la barra que aparece a la izquierda de cada línea revisada.
doc.layout_options.revision_options.inserted_text_color = aw.layout.RevisionColor.BRIGHT_GREEN
doc.layout_options.revision_options.show_revision_bars = False
doc.layout_options.revision_options.revision_bars_position = aw.drawing.HorizontalAlignment.RIGHT
doc.save(file_name=ARTIFACTS_DIR + 'Revision.LayoutOptionsRevisions.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

