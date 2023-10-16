---
title: Fill.fore_theme_color property
linktitle: fore_theme_color property
articleTitle: fore_theme_color property
second_title: Aspose.Words for Python
description: "Fill.fore_theme_color property. Gets or sets a ThemeColor object that represents the foreground color for the fill."
type: docs
weight: 80
url: /python-net/aspose.words.drawing/fill/fore_theme_color/
---

## Fill.fore_theme_color property

Gets or sets a ThemeColor object that represents the foreground color for the fill.


### Examples

Shows how to set theme color for foreground / background shape color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(awd.ShapeType.ROUND_RECTANGLE, 80.0, 80.0)

fill = shape.fill
fill.fore_theme_color = aw.themes.ThemeColor.DARK1
fill.back_theme_color = aw.themes.ThemeColor.BACKGROUND2

# Note: do not use "BackThemeColor" and "BackTintAndShade"for font fill.
if fill.back_tint_and_shade == 0:
    fill.back_tint_and_shade = 0.2

doc.save(ARTIFACTS_DIR + "Shape.FillThemeColor.docx");
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

