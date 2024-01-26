---
title: Stroke.back_theme_color property
linktitle: back_theme_color property
articleTitle: back_theme_color property
second_title: Aspose.Words for Python
description: "Stroke.back_theme_color property. Gets or sets a ThemeColor object that represents the stroke background color."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/stroke/back_theme_color/
---

## Stroke.back_theme_color property

Gets or sets a ThemeColor object that represents the stroke background color.


```python
@property
def back_theme_color(self) -> aspose.words.themes.ThemeColor:
    ...

@back_theme_color.setter
def back_theme_color(self, value: aspose.words.themes.ThemeColor):
    ...

```

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

