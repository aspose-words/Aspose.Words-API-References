---
title: Fill.back_tint_and_shade property
linktitle: back_tint_and_shade property
articleTitle: back_tint_and_shade property
second_title: Aspose.Words for Python
description: "Fill.back_tint_and_shade property. Gets or sets a double value that lightens or darkens the background color."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/fill/back_tint_and_shade/
---

## Fill.back_tint_and_shade property

Gets or sets a double value that lightens or darkens the background color.


```python
@property
def back_tint_and_shade(self) -> float:
    ...

@back_tint_and_shade.setter
def back_tint_and_shade(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.




### Examples

Shows how to set theme color for foreground/background shape color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.ROUND_RECTANGLE, width=80, height=80)
fill = shape.fill
fill.fore_theme_color = aw.themes.ThemeColor.DARK1
fill.back_theme_color = aw.themes.ThemeColor.BACKGROUND2
# Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
if fill.back_tint_and_shade == 0:
    fill.back_tint_and_shade = 0.2
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FillThemeColor.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

