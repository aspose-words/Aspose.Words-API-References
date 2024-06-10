---
title: Font.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "Font.kerning property. Gets or sets the font size at which kerning starts."
type: docs
weight: 180
url: /python-net/aspose.words/font/kerning/
---

## Font.kerning property

Gets or sets the font size at which kerning starts.


```python
@property
def kerning(self) -> float:
    ...

@kerning.setter
def kerning(self, value: float):
    ...

```

### Examples

Shows how to specify the font size at which kerning begins to take effect.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial Black'
# Set the builder's font size, and minimum size at which kerning will take effect.
# The font size falls below the kerning threshold, so the run bellow will not have kerning.
builder.font.size = 18
builder.font.kerning = 24
builder.writeln('TALLY. (Kerning not applied)')
# Set the kerning threshold so that the builder's current font size is above it.
# Any text we add from this point will have kerning applied. The spaces between characters
# will be adjusted, normally resulting in a slightly more aesthetically pleasing text run.
builder.font.kerning = 12
builder.writeln('TALLY. (Kerning applied)')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Kerning.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

