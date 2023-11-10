---
title: Font.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Python
description: "Font.spacing property. Returns or sets the spacing (in points) between characters ."
type: docs
weight: 380
url: /python-net/aspose.words/font/spacing/
---

## Font.spacing property

Returns or sets the spacing (in points) between characters .


```python
@property
def spacing(self) -> float:
    ...

@spacing.setter
def spacing(self, value: float):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add run of text and increase character width to 150%.
builder.font.scaling = 150
builder.writeln("Wide characters")

# Add run of text and add 1pt of extra horizontal spacing between each character.
builder.font.spacing = 1
builder.writeln("Expanded by 1pt")

# Add run of text and bring characters closer together by 1pt.
builder.font.spacing = -1
builder.writeln("Condensed by 1pt")

doc.save(ARTIFACTS_DIR + "Font.scaling_spacing.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

