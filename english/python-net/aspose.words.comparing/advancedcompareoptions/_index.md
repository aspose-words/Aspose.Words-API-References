---
title: AdvancedCompareOptions class
linktitle: AdvancedCompareOptions class
articleTitle: AdvancedCompareOptions class
second_title: Aspose.Words for Python
description: "aspose.words.comparing.AdvancedCompareOptions class. Allows to set advanced compare options."
type: docs
weight: 10
url: /python-net/aspose.words.comparing/advancedcompareoptions/
---

## AdvancedCompareOptions class

Allows to set advanced compare options.


### Remarks

These options have no equivalence in Microsoft Word and might help to produce more precise comparison result.


### Constructors
| Name | Description |
| --- | --- |
| [AdvancedCompareOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [ignore_dml_unique_id](./ignore_dml_unique_id/) | Specifies whether to ignore difference in DrawingML unique Id. |
| [ignore_store_item_id](./ignore_store_item_id/) | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |

### Examples

Shows how to compare SDT with same content but different store item id.

```python
doc_a = aw.Document(file_name=MY_DIR + 'Document with SDT 1.docx')
doc_b = aw.Document(file_name=MY_DIR + 'Document with SDT 2.docx')
# Configure options to compare SDT with same content but different store item id.
compare_options = aw.comparing.CompareOptions()
compare_options.advanced_options.ignore_store_item_id = False
doc_a.compare(document=doc_b, author='user', date_time=datetime.datetime.now(), options=compare_options)
self.assertEqual(8, doc_a.revisions.count)
compare_options.advanced_options.ignore_store_item_id = True
doc_a.revisions.reject_all()
doc_a.compare(document=doc_b, author='user', date_time=datetime.datetime.now(), options=compare_options)
self.assertEqual(0, doc_a.revisions.count)
```

### See Also

* module [aspose.words.comparing](../)

