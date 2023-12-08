---
title: Document.extract_pages method
linktitle: extract_pages method
articleTitle: extract_pages method
second_title: Aspose.Words for Python
description: "Document.extract_pages method. Returns the [Document](../) object representing specified range of pages."
type: docs
weight: 620
url: /python-net/aspose.words/document/extract_pages/
---

## extract_pages(index, count) {#int_int}

Returns the [Document](../) object representing specified range of pages.



```python
def extract_pages(self, index: int, count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


### Examples

Shows how to get specified range of pages from the document.

```python
doc = aw.Document(MY_DIR + "Layout entities.docx")

doc = doc.extract_pages(0, 2)

doc.save(ARTIFACTS_DIR + "Document.extract_pages.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

