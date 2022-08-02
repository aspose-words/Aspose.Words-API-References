---
title: EmphasisMark enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies possible types of emphasis mark."
type: docs
weight: 370
url: /python-net/aspose.words/emphasismark/
---

## EmphasisMark enumeration

Specifies possible types of emphasis mark.


### Members

| Name | Description |
| --- | --- |
| NONE | No emphasis mark. |
| OVER_SOLID_CIRCLE | Emphasis mark is a solid black circle displayed above text. |
| OVER_COMMA | Emphasis mark is a comma character displayed above text. |
| OVER_WHITE_CIRCLE | Emphasis mark is an empty white circle displayed above text. |
| UNDER_SOLID_CIRCLE | Emphasis mark is a solid black circle displayed below text. |

### Examples

Shows how to add additional character rendered above/below the glyph-character.

```python
builder = aw.DocumentBuilder()

# Possible types of emphasis mark:
# https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.font.emphasis_mark = emphasis_mark

builder.write("Emphasis text")
builder.writeln()
builder.font.clear_formatting()
builder.write("Simple text")

builder.document.save(ARTIFACTS_DIR + "Fonts.set_emphasis_mark.docx")
```

### See Also

* module [aspose.words](../)

