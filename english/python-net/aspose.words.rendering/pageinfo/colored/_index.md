---
title: PageInfo.colored property
linktitle: colored property
articleTitle: colored property
second_title: Aspose.Words for Python
description: "PageInfo.colored property. Returns ``True`` if the page contains colored content."
type: docs
weight: 10
url: /python-net/aspose.words.rendering/pageinfo/colored/
---

## PageInfo.colored property

Returns ``True`` if the page contains colored content.



### Examples

Shows how to check whether the page is in color or not.

```python
doc = aw.Document(MY_DIR + "Document.docx")

# Check that the first page of the document is not colored.
self.assertFalse(doc.get_page_info(0).colored)
```

### See Also

* module [aspose.words.rendering](../../)
* class [PageInfo](../)

