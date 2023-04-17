---
title: JustificationMode enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the character spacing adjustment for a document"
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
| EXPAND |  |
| COMPRESS |  |
| COMPRESS_KANA |  |

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

