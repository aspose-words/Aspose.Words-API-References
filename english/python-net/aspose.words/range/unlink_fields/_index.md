﻿---
title: unlink_fields method
second_title: Aspose.Words for Python via .NET API Reference
description: "Unlinks fields in this range."
type: docs
weight: 110
url: /python-net/aspose.words/range/unlink_fields/
---

## unlink_fields() {#default}

Unlinks fields in this range.


```python
def unlink_fields(self):
    ...
```

Replaces all the fields in this range with their most recent results.

To unlink fields in the whole document use [Range.unlink_fields()](./#default).




### Examples

Shows how to unlink all fields in a range.

```python
doc = aw.Document(MY_DIR + "Linked fields.docx")

new_section = doc.sections[0].clone(True).as_section()
doc.sections.add(new_section)

doc.sections[1].range.unlink_fields()
```

### See Also

* module [aspose.words](../../)
* class [Range](../)
