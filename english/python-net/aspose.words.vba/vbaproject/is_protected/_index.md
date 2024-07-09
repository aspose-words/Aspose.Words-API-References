---
title: VbaProject.is_protected property
linktitle: is_protected property
articleTitle: is_protected property
second_title: Aspose.Words for Python
description: "VbaProject.is_protected property. Shows whether the [VbaProject](../) is password protected."
type: docs
weight: 30
url: /python-net/aspose.words.vba/vbaproject/is_protected/
---

## VbaProject.is_protected property

Shows whether the [VbaProject](../) is password protected.



```python
@property
def is_protected(self) -> bool:
    ...

```

### Examples

Shows whether the VbaProject is password protected.

```python
doc = aw.Document(file_name=MY_DIR + 'Vba protected.docm')
self.assertTrue(doc.vba_project.is_protected)
```

### See Also

* module [aspose.words.vba](../../)
* class [VbaProject](../)

