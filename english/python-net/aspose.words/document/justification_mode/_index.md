---
title: Document.justification_mode property
linktitle: justification_mode property
articleTitle: justification_mode property
second_title: Aspose.Words for Python
description: "Document.justification_mode property. Gets or sets the character spacing adjustment of a document."
type: docs
weight: 230
url: /python-net/aspose.words/document/justification_mode/
---

## Document.justification_mode property

Gets or sets the character spacing adjustment of a document.


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

* module [aspose.words](../../)
* class [Document](../)

