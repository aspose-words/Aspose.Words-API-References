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


```python
@property
def locked(self) -> bool:
    ...

@locked.setter
def locked(self, value: bool):
    ...

```

### Examples

Shows how to lock style.

```python
doc = aw.Document()
style_heading1 = doc.styles.get_by_style_identifier(aw.StyleIdentifier.HEADING1)
if not style_heading1.locked:
    style_heading1.locked = True
doc.save(file_name=ARTIFACTS_DIR + 'Styles.LockStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

