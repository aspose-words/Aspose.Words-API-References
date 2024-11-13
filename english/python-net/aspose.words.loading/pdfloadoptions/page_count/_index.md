---
title: PdfLoadOptions.page_count property
linktitle: page_count property
articleTitle: page_count property
second_title: Aspose.Words for Python
description: "PdfLoadOptions.page_count property. Gets or sets the number of pages to read"
type: docs
weight: 20
url: /python-net/aspose.words.loading/pdfloadoptions/page_count/
---

## PdfLoadOptions.page_count property

Gets or sets the number of pages to read. Default is MaxValue which means all pages of the document will be read.


```python
@property
def page_count(self) -> int:
    ...

@page_count.setter
def page_count(self, value: int):
    ...

```

### Examples

Shows how to skip images during loading PDF files.

```python
options = aw.loading.PdfLoadOptions()
options.skip_pdf_images = is_skip_pdf_images
options.page_index = 0
options.page_count = 1
doc = aw.Document(file_name=MY_DIR + 'Images.pdf', load_options=options)
shape_collection = doc.get_child_nodes(aw.NodeType.SHAPE, True)
if is_skip_pdf_images:
    self.assertEqual(shape_collection.count, 0)
else:
    self.assertNotEqual(shape_collection.count, 0)
```

### See Also

* module [aspose.words.loading](../../)
* class [PdfLoadOptions](../)

