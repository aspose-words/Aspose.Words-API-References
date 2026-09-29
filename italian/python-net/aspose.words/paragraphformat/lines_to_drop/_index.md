---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /it/python-net/aspose.words/paragraphformat/lines_to_drop/
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
# Modifica la proprietà "LinesToDrop" per designare un paragrafo come capoverso iniziale,
# che lo trasformerà in una grande lettera maiuscola che decorerà il paragrafo successivo.
# Assegna a questa proprietà il valore 4 per impostare l'altezza della lettera iniziale a quattro righe di testo.
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# Reimposta la proprietà "LinesToDrop" a 0 per trasformare il paragrafo successivo in un paragrafo ordinario.
# Il testo in questo paragrafo avvolgerà la lettera iniziale.
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

