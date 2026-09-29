---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /it/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Il costruttore di documenti ha un cursore, che funge da parte del documento
# dove il costruttore aggiunge nuovi nodi quando utilizziamo i suoi metodi di costruzione del documento.
# Questo cursore funziona allo stesso modo del cursore lampeggiante di Microsoft Word,
# e finisce sempre immediatamente dopo qualsiasi nodo che il costruttore ha appena inserito.
# Per aggiungere contenuto a una parte diversa del documento,
# possiamo spostare il cursore su un nodo diverso con il metodo "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Il cursore è ora davanti al nodo a cui lo abbiamo spostato.
# Aggiungere una seconda sequenza la inserirà davanti alla prima sequenza.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Sposta il cursore alla fine del documento per continuare ad aggiungere testo alla fine come prima.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

