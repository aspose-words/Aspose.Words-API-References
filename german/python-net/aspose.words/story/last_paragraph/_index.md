---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /de/python-net/aspose.words/story/last_paragraph/
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
# Der Dokumenten-Builder hat einen Cursor, der als Teil des Dokuments fungiert
# wo der Builder neue Knoten anhängt, wenn wir seine Dokumentenkonstruktionsmethoden verwenden.
# Dieser Cursor funktioniert auf die gleiche Weise wie der blinkende Cursor von Microsoft Word,
# und er endet außerdem immer unmittelbar nach jedem Knoten, den der Builder gerade eingefügt hat.
# Um Inhalt an einem anderen Teil des Dokuments anzuhängen,
# können wir den Cursor mit der Methode "MoveTo" zu einem anderen Knoten bewegen.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Der Cursor befindet sich jetzt vor dem Knoten, zu dem wir ihn bewegt haben.
# Das Hinzufügen eines zweiten Laufs wird ihn vor dem ersten Lauf einfügen.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Bewegen Sie den Cursor ans Ende des Dokuments, um das Anfügen von Text am Ende wie zuvor fortzusetzen.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

