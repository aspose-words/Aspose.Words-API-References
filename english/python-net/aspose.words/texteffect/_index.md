---
title: TextEffect enumeration
linktitle: TextEffect enumeration
articleTitle: TextEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TextEffect enumeration. Animation effect for text runs."
type: docs
weight: 1320
url: /python-net/aspose.words/texteffect/
---

## TextEffect enumeration

Animation effect for text runs.


### Members

| Name | Description |
| --- | --- |
| NONE |  |
| LAS_VEGAS_LIGHTS |  |
| BLINKING_BACKGROUND |  |
| SPARKLE_TEXT |  |
| MARCHING_BLACK_ANTS |  |
| MARCHING_RED_ANTS |  |
| SHIMMER |  |

### Examples

Shows how to apply a visual effect to a run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 36
builder.font.text_effect = aw.TextEffect.SPARKLE_TEXT
builder.writeln('Text with a sparkle effect.')
# Older versions of Microsoft Word only support font animation effects.
doc.save(file_name=ARTIFACTS_DIR + 'Font.SparklingText.doc')
```

### See Also

* module [aspose.words](../)

