---
title: FontInfo.panose property
linktitle: panose property
articleTitle: panose property
second_title: Aspose.Words for Python
description: "FontInfo.panose property. Gets or sets the PANOSE typeface classification number."
type: docs
weight: 70
url: /python-net/aspose.words.fonts/fontinfo/panose/
---

## FontInfo.panose property

Gets or sets the PANOSE typeface classification number.


```python
@property
def panose(self) -> bytes:
    ...

@panose.setter
def panose(self, value: bytes):
    ...

```

### Remarks

PANOSE is a compact 10-byte description of a fonts critical visual characteristics,
such as contrast, weight, and serif style. The digits represent Family Kind, Serif Style,
Weight, Proportion, Contrast, Stroke Variation, Arm Style, Letterform, Midline, and X-Height.

Can be ``None``.




### See Also

* module [aspose.words.fonts](../../)
* class [FontInfo](../)

