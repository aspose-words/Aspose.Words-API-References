---
title: Shading.background_pattern_theme_color property
linktitle: background_pattern_theme_color property
articleTitle: background_pattern_theme_color property
second_title: Aspose.Words for Python
description: "Shading.background_pattern_theme_color property. Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../) object."
type: docs
weight: 20
url: /python-net/aspose.words/shading/background_pattern_theme_color/
---

## Shading.background_pattern_theme_color property

Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../) object.



```python
@property
def background_pattern_theme_color(self) -> aspose.words.themes.ThemeColor:
    ...

@background_pattern_theme_color.setter
def background_pattern_theme_color(self, value: aspose.words.themes.ThemeColor):
    ...

```

### Examples

Shows how to set foreground and background colors for shading texture.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shading = doc.first_section.body.first_paragraph.paragraph_format.shading
shading.texture = aw.TextureIndex.TEXTURE_12PT5_PERCENT
shading.foreground_pattern_theme_color = aw.themes.ThemeColor.DARK1
shading.background_pattern_theme_color = aw.themes.ThemeColor.DARK2
shading.foreground_tint_and_shade = 0.5
shading.background_tint_and_shade = -0.2
builder.font.border.color = aspose.pydrawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER
builder.writeln('Foreground and background pattern colors for shading texture.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ForegroundAndBackground.docx')
```

### See Also

* module [aspose.words](../../)
* class [Shading](../)

