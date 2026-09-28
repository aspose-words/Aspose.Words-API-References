---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /de/python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ändern Sie die Eigenschaft "LinesToDrop", um einen Absatz als Initialbuchstaben zu kennzeichnen,
# die es in einen großen Großbuchstaben verwandelt, der den nächsten Absatz schmückt.
# Setzen Sie diese Eigenschaft auf den Wert 4, um dem Initialbuchstaben die Höhe von vier Textzeilen zu geben.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Setzen Sie die Eigenschaft "LinesToDrop" auf 0 zurück, um den nächsten Absatz in einen normalen Absatz zu verwandeln.
# Der Text in diesem Absatz wird um den Initialbuchstaben fließen.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

