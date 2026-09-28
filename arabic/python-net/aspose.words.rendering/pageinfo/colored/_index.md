---
title: PageInfo.colored property
linktitle: colored property
articleTitle: colored property
second_title: Aspose.Words for Python
description: "PageInfo.colored property. Returns ``True`` if the page contains colored content."
type: docs
weight: 10
url: /ar/python-net/aspose.words.rendering/pageinfo/colored/
---

## PageInfo.colored property

Returns ``True`` if the page contains colored content.



```python
@property
def colored(self) -> bool:
    ...

```

### Examples

Shows how to check whether the page is in color or not.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# تحقق من أن الصفحة الأولى من المستند غير ملونة.
self.assertFalse(doc.get_page_info(0).colored)
```

### See Also

* module [aspose.words.rendering](../../)
* class [PageInfo](../)

