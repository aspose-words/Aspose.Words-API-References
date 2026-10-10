---
title: ParagraphFormat.right_indent property
linktitle: right_indent property
articleTitle: right_indent property
second_title: Aspose.Words for Python
description: "ParagraphFormat.right_indent property. Gets or sets the value (in points) that represents the right indent for paragraph."
type: docs
weight: 280
url: /fr/python-net/aspose.words/paragraphformat/right_indent/
---

## ParagraphFormat.right_indent property

Gets or sets the value (in points) that represents the right indent for paragraph.


```python
@property
def right_indent(self) -> float:
    ...

@right_indent.setter
def right_indent(self, value: float):
    ...

```

### Examples

Shows how to configure paragraph formatting to create off-center text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Centrer tout le texte que le constructeur de document écrit, et définir les retraits.
# La configuration de retrait ci-dessous créera un corps de texte qui sera placé de manière asymétrique sur la page.
# Le "centre" auquel nous alignons le texte sera le milieu du corps de texte, pas le milieu de la page.
paragraph_format = builder.paragraph_format
paragraph_format.alignment = aw.ParagraphAlignment.CENTER
paragraph_format.left_indent = 100
paragraph_format.right_indent = 50
paragraph_format.space_after = 25
builder.writeln('This paragraph demonstrates how left and right indentation affects word wrapping.')
builder.writeln("The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.")
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetParagraphFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

