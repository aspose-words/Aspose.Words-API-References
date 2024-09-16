---
title: TextDmlEffect enumeration
linktitle: TextDmlEffect enumeration
articleTitle: TextDmlEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TextDmlEffect enumeration. Dml text effect for text runs."
type: docs
weight: 1260
url: /python-net/aspose.words/textdmleffect/
---

## TextDmlEffect enumeration

Dml text effect for text runs.


### Members

| Name | Description |
| --- | --- |
| GLOW | Glow effect, in which a color blurred outline is added outside the edges of the object. |
| FILL | Fill overlay effect. |
| SHADOW | Shadow effect. |
| OUTLINE | Outline effect. |
| EFFECT_3D | 3D effect. |
| REFLECTION | Reflection effect. |

### Examples

Shows how to check if a run displays a DrawingML text effect.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML text effects.docx')
runs = doc.first_section.body.first_paragraph.runs
self.assertTrue(runs[0].font.has_dml_effect(aw.TextDmlEffect.SHADOW))
self.assertTrue(runs[1].font.has_dml_effect(aw.TextDmlEffect.SHADOW))
self.assertTrue(runs[2].font.has_dml_effect(aw.TextDmlEffect.REFLECTION))
self.assertTrue(runs[3].font.has_dml_effect(aw.TextDmlEffect.EFFECT_3D))
self.assertTrue(runs[4].font.has_dml_effect(aw.TextDmlEffect.FILL))
```

### See Also

* module [aspose.words](../)

