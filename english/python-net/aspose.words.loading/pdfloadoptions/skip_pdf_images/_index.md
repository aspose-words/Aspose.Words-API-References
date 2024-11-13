---
title: PdfLoadOptions.skip_pdf_images property
linktitle: skip_pdf_images property
articleTitle: skip_pdf_images property
second_title: Aspose.Words for Python
description: "PdfLoadOptions.skip_pdf_images property. Gets or sets the flag indicating whether images must be skipped while loading PDF document"
type: docs
weight: 40
url: /python-net/aspose.words.loading/pdfloadoptions/skip_pdf_images/
---

## PdfLoadOptions.skip_pdf_images property

Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is ``False``.



```python
@property
def skip_pdf_images(self) -> bool:
    ...

@skip_pdf_images.setter
def skip_pdf_images(self, value: bool):
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

