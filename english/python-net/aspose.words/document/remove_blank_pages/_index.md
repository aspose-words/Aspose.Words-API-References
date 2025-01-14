---
title: Document.remove_blank_pages method
linktitle: remove_blank_pages method
articleTitle: remove_blank_pages method
second_title: Aspose.Words for Python
description: "Document.remove_blank_pages method. Removes blank pages from the document."
type: docs
weight: 690
url: /python-net/aspose.words/document/remove_blank_pages/
---

## remove_blank_pages() {#default}

Removes blank pages from the document.


```python
def remove_blank_pages(self):
    ...
```

### Remarks

The resulting document will not contain pages considered to be blank while other content,
including numbering, headers/footers and overall layout should remain unchanged.

Page is considered to be blank when body of the page have no visible content, for example,
empty table having no borders will be considered as invisible and therefore page will be detected as blank.


### Returns

List of page numbers has been considered as blank and removed.


### Examples

Shows how to remove blank pages from the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Blank pages.docx')
self.assertEqual(2, doc.page_count)
doc.remove_blank_pages()
doc.update_page_layout()
self.assertEqual(1, doc.page_count)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

