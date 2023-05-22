---
title: Shading.foreground_tint_and_shade property
linktitle: foreground_tint_and_shade property
articleTitle: foreground_tint_and_shade property
second_title: Aspose.Words for Python
description: "Shading.foreground_tint_and_shade property. Gets or sets a double value that lightens or darkens a foreground theme color."
type: docs
weight: 60
url: /python-net/aspose.words/shading/foreground_tint_and_shade/
---

## Shading.foreground_tint_and_shade property

Gets or sets a double value that lightens or darkens a foreground theme color.

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.
Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1
results in System.ArgumentOutOfRangeException.

Setting this property for Shading object with non-theme colors
results in System.InvalidOperationException.




### Examples

Shows how to set foreground and background colors for shading texture.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shading = doc.first_section.body.first_paragraph.paragraph_format.shading
shading.texture = aw.TextureIndex.TEXTURE_12PT5_PERCENT
shading.foreground_pattern_theme_color = aw.themes.ThemeColor.DARK1
shading.background_pattern_theme_color = aw.themes.ThemeColor.DARK2

shading.foreground_tint_and_shade = 0.5
shading.background_tint_and_shade = -0.2

builder.font.border.color = drawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER

builder.writeln("Foreground and background pattern colors for shading texture.")

doc.save(ARTIFACTS_DIR + "Font.ForegroundAndBackground.docx")
```

### See Also

* module [aspose.words](../../)
* class [Shading](../)

