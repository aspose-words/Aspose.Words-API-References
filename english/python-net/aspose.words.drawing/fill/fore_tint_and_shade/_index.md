---
title: Fill.fore_tint_and_shade property
linktitle: fore_tint_and_shade property
articleTitle: fore_tint_and_shade property
second_title: Aspose.Words for Python
description: "Fill.fore_tint_and_shade property. Gets or sets a double value that lightens or darkens the foreground color."
type: docs
weight: 90
url: /python-net/aspose.words.drawing/fill/fore_tint_and_shade/
---

## Fill.fore_tint_and_shade property

Gets or sets a double value that lightens or darkens the foreground color.


```python
@property
def fore_tint_and_shade(self) -> float:
    ...

@fore_tint_and_shade.setter
def fore_tint_and_shade(self, value: float):
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

Shows how to manage lightening and darkening foreground font color.

```python
doc = aw.Document(MY_DIR + "Big document.docx")

text_fill = doc.first_section.body.first_paragraph.runs[0].font.fill
text_fill.fore_theme_color = aw.themes.ThemeColor.ACCENT1
if text_fill.fore_tint_and_shade == 0:
    text_fill.fore_tint_and_shade = 0.5

doc.save(ARTIFACTS_DIR + "Shape.FillTintAndShade.docx");
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

