---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /de/python-net/aspose.words/paragraphformat/outline_level/
---

## ParagraphFormat.outline_level property

Specifies the outline level of the paragraph in the document.


```python
@property
def outline_level(self) -> aspose.words.OutlineLevel:
    ...

@outline_level.setter
def outline_level(self, value: aspose.words.OutlineLevel):
    ...

```

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Jeder Absatz hat ein OutlineLevel, das jede Zahl von 1 bis 9 sein kann oder den Standardwert "BodyText".
# Das Festlegen der Eigenschaft auf einen der nummerierten Werte zeigt einen Pfeil nach links.
# am Anfang des Absatzes.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Level 1 ist die höchste Ebene. Wenn ein Absatz mit einer niedrigeren Ebene unter einem Absatz mit einer höheren Ebene liegt,
# wird das Zusammenklappen des Absatzes mit höherer Ebene den Absatz mit niedrigerer Ebene zusammenklappen.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Zwei Absätze derselben Ebene werden einander nicht zusammenklappen,
# und die Pfeile klappen die Absätze, auf die sie zeigen, nicht zusammen.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# Der Standardwert "BodyText" ist der niedrigste, den ein Absatz jeder Ebene zusammenklappen kann.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

