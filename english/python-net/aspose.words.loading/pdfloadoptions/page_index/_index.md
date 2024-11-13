---
title: PdfLoadOptions.page_index property
linktitle: page_index property
articleTitle: page_index property
second_title: Aspose.Words for Python
description: "PdfLoadOptions.page_index property. Gets or sets the 0-based index of the first page to read"
type: docs
weight: 30
url: /python-net/aspose.words.loading/pdfloadoptions/page_index/
---

## PdfLoadOptions.page_index property

Gets or sets the 0-based index of the first page to read. Default is 0.


```python
@property
def page_index(self) -> int:
    ...

@page_index.setter
def page_index(self, value: int):
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

