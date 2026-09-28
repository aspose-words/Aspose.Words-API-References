---
title: OutlineLevel enumeration
linktitle: OutlineLevel enumeration
articleTitle: OutlineLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.OutlineLevel enumeration. Specifies the outline level of a paragraph in the document."
type: docs
weight: 890
url: /de/python-net/aspose.words/outlinelevel/
---

## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.


### Members

| Name | Description |
| --- | --- |
| LEVEL1 | The paragraph is at the outline level 1 (topmost level). |
| LEVEL2 | The paragraph is at the outline level 2. |
| LEVEL3 | The paragraph is at the outline level 3. |
| LEVEL4 | The paragraph is at the outline level 4. |
| LEVEL5 | The paragraph is at the outline level 5. |
| LEVEL6 | The paragraph is at the outline level 6. |
| LEVEL7 | The paragraph is at the outline level 7. |
| LEVEL8 | The paragraph is at the outline level 8. |
| LEVEL9 | The paragraph is at the outline level 9. |
| BODY_TEXT | The paragraph is at the level of the main text. |

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

* module [aspose.words](../)

