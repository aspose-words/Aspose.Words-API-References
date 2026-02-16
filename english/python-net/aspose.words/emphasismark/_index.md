---
title: EmphasisMark enumeration
linktitle: EmphasisMark enumeration
articleTitle: EmphasisMark enumeration
second_title: Aspose.Words for Python
description: "aspose.words.EmphasisMark enumeration. Specifies possible types of emphasis mark."
type: docs
weight: 400
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
# https:#apireference.aspose.com/words/net/aspose.words/emphasismark
builder.font.emphasis_mark = emphasis_mark
builder.write('Emphasis text')
builder.writeln()
builder.font.clear_formatting()
builder.write('Simple text')
builder.document.save(file_name=ARTIFACTS_DIR + 'Fonts.SetEmphasisMark.docx')
```

### See Also

* module [aspose.words](../)

