---
title: CompareOptions.ignore_dml_unique_id property
linktitle: ignore_dml_unique_id property
articleTitle: ignore_dml_unique_id property
second_title: Aspose.Words for Python
description: "CompareOptions.ignore_dml_unique_id property. Specifies whether to ignore difference in DrawingML unique Id."
type: docs
weight: 70
url: /python-net/aspose.words.comparing/compareoptions/ignore_dml_unique_id/
---

## CompareOptions.ignore_dml_unique_id property

Specifies whether to ignore difference in DrawingML unique Id.


```python
@property
def ignore_dml_unique_id(self) -> bool:
    ...

@ignore_dml_unique_id.setter
def ignore_dml_unique_id(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to compare documents ignoring DML unique ID.

```python
doc_a = aw.Document(MY_DIR + 'DML unique ID original.docx')
doc_b = aw.Document(MY_DIR + 'DML unique ID compare.docx')
# By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
# If we are ignoring DML's unique ID, and revisions count were 0.
compare_options = aw.comparing.CompareOptions()
compare_options.ignore_dml_unique_id = is_ignore_dml_unique_id
doc_a.compare(doc_b, 'Aspose.Words', datetime.datetime.now(), compare_options)
self.assertEqual(0 if is_ignore_dml_unique_id else 2, doc_a.revisions.count)
```

### See Also

* module [aspose.words.comparing](../../)
* class [CompareOptions](../)

