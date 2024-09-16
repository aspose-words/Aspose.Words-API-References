---
title: Font.tint_and_shade property
linktitle: tint_and_shade property
articleTitle: tint_and_shade property
second_title: Aspose.Words for Python
description: "Font.tint_and_shade property. Gets or sets a double value that lightens or darkens a color."
type: docs
weight: 520
url: /python-net/aspose.words/font/tint_and_shade/
---

## Font.tint_and_shade property

Gets or sets a double value that lightens or darkens a color.


```python
@property
def tint_and_shade(self) -> float:
    ...

@tint_and_shade.setter
def tint_and_shade(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if set this property for [Font](../) object with non-theme colors. |

### Remarks

The allowed values are in range from -1 (darkest) to 1 (lightest) for this property.

Zero (0) is neutral.




### Examples

Shows how to create and use themed style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln()
# Create some style with theme font properties.
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'ThemedStyle')
style.font.theme_font = aw.themes.ThemeFont.MAJOR
style.font.theme_color = aw.themes.ThemeColor.ACCENT5
style.font.tint_and_shade = 0.3
builder.paragraph_format.style_name = 'ThemedStyle'
builder.writeln('Text with themed style')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

