---
title: Stroke.back_tint_and_shade property
linktitle: back_tint_and_shade property
articleTitle: back_tint_and_shade property
second_title: Aspose.Words for Python
description: "Stroke.back_tint_and_shade property. Gets or sets a double value that lightens or darkens the stroke background color."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/stroke/back_tint_and_shade/
---

## Stroke.back_tint_and_shade property

Gets or sets a double value that lightens or darkens the stroke background color.


```python
@property
def back_tint_and_shade(self) -> float:
    ...

@back_tint_and_shade.setter
def back_tint_and_shade(self, value: float):
    ...

```

### Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property.
Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1
results in System.ArgumentOutOfRangeException.




### Examples

Shows how to set back theme color and tint and shade.

```python
doc = aw.Document(MY_DIR + "Stroke gradient outline.docx")

shape = doc.get_child(NodeType.SHAPE, 0, True).as_shape()
stroke = shape.stroke
stroke.back_theme_color = ThemeColor.DARK2
stroke.back_tint_and_shade = 0.2

doc.save(ARTIFACTS_DIR + "Shape.StrokeBackThemeColors.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

