---
title: ParagraphFormat.outline_level property
linktitle: outline_level property
articleTitle: outline_level property
second_title: Aspose.Words for Python
description: "ParagraphFormat.outline_level property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /sv/python-net/aspose.words/paragraphformat/outline_level/
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
# Varje stycke har en OutlineLevel, som kan vara vilket tal som helst från 1 till 9, eller vid standardvärdet "BodyText".
# Att sätta egenskapen till ett av de numrerade värdena visar en pil åt vänster
# vid början av stycket.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL1
builder.writeln('Paragraph outline level 1.')
# Nivå 1 är den högsta nivån. Om det finns ett stycke med en lägre nivå under ett stycke med en högre nivå,
# kommer kollapsning av det högre nivåstycket att kollapsa det lägre nivåstycket.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL2
builder.writeln('Paragraph outline level 2.')
# Två stycken på samma nivå kommer inte att kollapsa varandra,
# och pilarna kollapsar inte de stycken de pekar på.
builder.paragraph_format.outline_level = aw.OutlineLevel.LEVEL3
builder.writeln('Paragraph outline level 3.')
builder.writeln('Paragraph outline level 3.')
# Standardvärdet "BodyText" är det lägsta, som ett stycke på vilken nivå som helst kan kollapsa.
builder.paragraph_format.outline_level = aw.OutlineLevel.BODY_TEXT
builder.writeln('Paragraph at main text level.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphOutlineLevel.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

