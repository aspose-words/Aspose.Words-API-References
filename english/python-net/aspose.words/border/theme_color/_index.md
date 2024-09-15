---
title: Border.theme_color property
linktitle: theme_color property
articleTitle: theme_color property
second_title: Aspose.Words for Python
description: "Border.theme_color property. Gets or sets the theme color in the applied color scheme that is associated with this Border object."
type: docs
weight: 70
url: /python-net/aspose.words/border/theme_color/
---

## Border.theme_color property

Gets or sets the theme color in the applied color scheme that is associated with this Border object.


```python
@property
def theme_color(self) -> aspose.words.themes.ThemeColor:
    ...

@theme_color.setter
def theme_color(self, value: aspose.words.themes.ThemeColor):
    ...

```

### Examples

Shows how to insert a paragraph with a top border.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
top_border = builder.paragraph_format.borders.top
top_border.line_width = 4
top_border.line_style = aw.LineStyle.DASH_SMALL_GAP
# Set ThemeColor only when LineWidth or LineStyle setted.
top_border.theme_color = aw.themes.ThemeColor.ACCENT1
top_border.tint_and_shade = 0.25
builder.writeln('Text with a top border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.ParagraphTopBorder.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

