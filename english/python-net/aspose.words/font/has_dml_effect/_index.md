---
title: has_dml_effect method
second_title: Aspose.Words for Python via .NET API Reference
description: "Checks if particular DrawingML text effect is applied."
type: docs
weight: 560
url: /python-net/aspose.words/font/has_dml_effect/
---

## has_dml_effect(dml_effect_type) {#textdmleffect}

Checks if particular DrawingML text effect is applied.


```python
def has_dml_effect(self, dml_effect_type: aspose.words.TextDmlEffect):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| dml_effect_type | [TextDmlEffect](../../textdmleffect/) |  |

### Returns

``True`` if particular DrawingML text effect is applied.


### Examples

Shows how to check if a run displays a DrawingML text effect.

```python
doc = aw.Document(MY_DIR + "DrawingML text effects.docx")

runs = doc.first_section.body.first_paragraph.runs

self.assertTrue(runs[0].font.has_dml_effect(aw.TextDmlEffect.SHADOW))
self.assertTrue(runs[1].font.has_dml_effect(aw.TextDmlEffect.SHADOW))
self.assertTrue(runs[2].font.has_dml_effect(aw.TextDmlEffect.REFLECTION))
self.assertTrue(runs[3].font.has_dml_effect(aw.TextDmlEffect.EFFECT_3D))
self.assertTrue(runs[4].font.has_dml_effect(aw.TextDmlEffect.FILL))
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

