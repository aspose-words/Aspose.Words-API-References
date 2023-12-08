---
title: JustificationMode enumeration
linktitle: JustificationMode enumeration
articleTitle: JustificationMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.JustificationMode enumeration. Specifies the character spacing adjustment for a document"
type: docs
weight: 40
url: /python-net/aspose.words.settings/justificationmode/
---

## JustificationMode enumeration

Specifies the character spacing adjustment for a document.
The default value is ``Expand``.



### Members

| Name | Description |
| --- | --- |
| EXPAND | Do not compress character spacing. |
| COMPRESS | Compress character spacing. |
| COMPRESS_KANA | Compress, using rules of the kana syllabaries, Hiragana and Katakana. |

### Examples

Shows how to manage character spacing control.

```python
doc = aw.Document(MY_DIR + "Document.docx")
justification_mode = doc.justification_mode
if justification_mode == aw.settings.JustificationMode.EXPAND:
    doc.justification_mode = aw.settings.JustificationMode.COMPRESS

doc.save(ARTIFACTS_DIR + "Document.SetJustificationMode.docx")
```

### See Also

* module [aspose.words.settings](../)

