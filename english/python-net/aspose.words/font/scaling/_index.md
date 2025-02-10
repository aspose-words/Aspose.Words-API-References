---
title: Font.scaling property
linktitle: scaling property
articleTitle: scaling property
second_title: Aspose.Words for Python
description: "Font.scaling property. Gets or sets character width scaling in percent."
type: docs
weight: 320
url: /python-net/aspose.words/font/scaling/
---

## Font.scaling property

Gets or sets character width scaling in percent.


```python
@property
def scaling(self) -> int:
    ...

@scaling.setter
def scaling(self, value: int):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Add run of text and increase character width to 150%.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Add run of text and add 1pt of extra horizontal spacing between each character.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Add run of text and bring characters closer together by 1pt.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

