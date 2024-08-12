---
title: Document.get_page_info method
linktitle: get_page_info method
articleTitle: get_page_info method
second_title: Aspose.Words for Python
description: "Document.get_page_info method. Gets the page size, orientation and other information about a page that might be useful for printing or rendering."
type: docs
weight: 650
url: /python-net/aspose.words/document/get_page_info/
---

## get_page_info(page_index) {#int}

Gets the page size, orientation and other information about a page that might be useful for printing or rendering.


```python
def get_page_info(self, page_index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| page_index | int | The 0-based page index. |

### Examples

Shows how to check whether the page is in color or not.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# Check that the first page of the document is not colored.
self.assertFalse(doc.get_page_info(0).colored)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

