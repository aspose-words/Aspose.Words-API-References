---
title: Style.locked property
linktitle: locked property
articleTitle: locked property
second_title: Aspose.Words for Python
description: "Style.locked property. Specifies whether this style is locked."
type: docs
weight: 120
url: /python-net/aspose.words/style/locked/
---

## Style.locked property

Specifies whether this style is locked.


### Examples

Shows how to lock style.

```python
doc = aw.Document()

style_heading_1 = doc.styles[aw.StyleIdentifier.HEADING1]
if not style_heading_1.locked:
    style_heading_1.locked = True

doc.save(ARTIFACTS_DIR + "Styles.LockStyle.docx")
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

