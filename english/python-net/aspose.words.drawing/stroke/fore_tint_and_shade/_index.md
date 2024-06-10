---
title: Stroke.fore_tint_and_shade property
linktitle: fore_tint_and_shade property
articleTitle: fore_tint_and_shade property
second_title: Aspose.Words for Python
description: "Stroke.fore_tint_and_shade property. Gets or sets a double value that lightens or darkens the stroke foreground color."
type: docs
weight: 150
url: /python-net/aspose.words.drawing/stroke/fore_tint_and_shade/
---

## Stroke.fore_tint_and_shade property

Gets or sets a double value that lightens or darkens the stroke foreground color.


```python
@property
def fore_tint_and_shade(self) -> float:
    ...

@fore_tint_and_shade.setter
def fore_tint_and_shade(self, value: float):
    ...

```

### Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property.
Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1
results in System.ArgumentOutOfRangeException.




### Examples

Shows how to set fore theme color and tint and shade.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=40)
stroke = shape.stroke
stroke.fore_theme_color = aw.themes.ThemeColor.DARK1
stroke.fore_tint_and_shade = 0.5
doc.save(file_name=ARTIFACTS_DIR + 'Shape.StrokeForeThemeColors.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

