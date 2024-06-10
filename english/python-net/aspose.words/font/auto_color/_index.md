---
title: Font.auto_color property
linktitle: auto_color property
articleTitle: auto_color property
second_title: Aspose.Words for Python
description: "Font.auto_color property. Returns the present calculated color of the text (black or white) to be used for 'auto color'"
type: docs
weight: 20
url: /python-net/aspose.words/font/auto_color/
---

## Font.auto_color property

Returns the present calculated color of the text (black or white) to be used for 'auto color'.
If the color is not 'auto' then returns [Font.color](../color/).



```python
@property
def auto_color(self) -> aspose.pydrawing.Color:
    ...

```

### Remarks

When text has 'automatic color', the actual color of text is calculated automatically
so that it is readable against the background color. As you change the background color,
the text color will automatically switch to black or white in MS Word to maximize legibility.




### Examples

Shows how to improve readability by automatically selecting text color based on the brightness of its background.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# If a run's Font object does not specify text color, it will automatically
# select either black or white depending on the background color's color.
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), builder.font.color.to_argb())
# The default color for text is black. If the color of the background is dark, black text will be difficult to see.
# To solve this problem, the AutoColor property will display this text in white.
builder.font.shading.background_pattern_color = aspose.pydrawing.Color.dark_blue
builder.writeln('The text color automatically chosen for this run is white.')
self.assertEqual(aspose.pydrawing.Color.white.to_argb(), doc.first_section.body.paragraphs[0].runs[0].font.auto_color.to_argb())
# If we change the background to a light color, black will be a more
# suitable text color than white so that the auto color will display it in black.
builder.font.shading.background_pattern_color = aspose.pydrawing.Color.light_blue
builder.writeln('The text color automatically chosen for this run is black.')
self.assertEqual(aspose.pydrawing.Color.black.to_argb(), doc.first_section.body.paragraphs[1].runs[0].font.auto_color.to_argb())
doc.save(file_name=ARTIFACTS_DIR + 'Font.SetFontAutoColor.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

