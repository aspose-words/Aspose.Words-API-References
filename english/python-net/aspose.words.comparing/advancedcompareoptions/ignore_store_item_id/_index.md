---
title: AdvancedCompareOptions.ignore_store_item_id property
linktitle: ignore_store_item_id property
articleTitle: ignore_store_item_id property
second_title: Aspose.Words for Python
description: "AdvancedCompareOptions.ignore_store_item_id property. Specifies whether to ignore difference in StructuredDocumentTag store item Id."
type: docs
weight: 30
url: /python-net/aspose.words.comparing/advancedcompareoptions/ignore_store_item_id/
---

## AdvancedCompareOptions.ignore_store_item_id property

Specifies whether to ignore difference in StructuredDocumentTag store item Id.


```python
@property
def ignore_store_item_id(self) -> bool:
    ...

@ignore_store_item_id.setter
def ignore_store_item_id(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to compare SDT with same content but different store item id.

```python
doc_a = aw.Document(file_name=MY_DIR + 'Document with SDT 1.docx')
doc_b = aw.Document(file_name=MY_DIR + 'Document with SDT 2.docx')
# Configure options to compare SDT with same content but different store item id.
compare_options = aw.comparing.CompareOptions()
compare_options.advanced_options.ignore_store_item_id = False
doc_a.compare(doc_b, "user", datetime.now(), compare_options)
self.assertEqual(8, doc_a.revisions.count)
compare_options.advanced_options.ignore_store_item_id = True
doc_a.revisions.reject_all()
doc_a.compare(doc_b, "user", datetime.now(), compare_options)
self.assertEqual(0, doc_a.revisions.count)
```

### See Also

* module [aspose.words.comparing](../../)
* class [AdvancedCompareOptions](../)

