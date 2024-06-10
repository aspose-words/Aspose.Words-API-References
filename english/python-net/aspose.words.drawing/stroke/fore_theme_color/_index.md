---
title: Stroke.fore_theme_color property
linktitle: fore_theme_color property
articleTitle: fore_theme_color property
second_title: Aspose.Words for Python
description: "Stroke.fore_theme_color property. Gets or sets a ThemeColor object that represents the stroke foreground color."
type: docs
weight: 140
url: /python-net/aspose.words.drawing/stroke/fore_theme_color/
---

## Stroke.fore_theme_color property

Gets or sets a ThemeColor object that represents the stroke foreground color.


```python
@property
def fore_theme_color(self) -> aspose.words.themes.ThemeColor:
    ...

@fore_theme_color.setter
def fore_theme_color(self, value: aspose.words.themes.ThemeColor):
    ...

```

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

