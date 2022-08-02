---
title: unlink method
second_title: Aspose.Words for Python via .NET API Reference
description: "Performs the field unlink."
type: docs
weight: 1080
url: /python-net/aspose.words.fields/field/unlink/
---

## unlink() {#default}

Performs the field unlink.


```python
def unlink(self):
    ...
```

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.




### Returns

``True`` if the field has been unlinked, otherwise ``false``.



### Examples

Shows how to unlink a field.

```python
doc = aw.Document(MY_DIR + "Linked fields.docx")
doc.range.fields[1].unlink()
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

