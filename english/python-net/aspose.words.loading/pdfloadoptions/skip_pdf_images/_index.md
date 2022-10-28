---
title: skip_pdf_images property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the flag indicating whether images must be skipped while loading PDF document"
type: docs
weight: 40
url: /python-net/aspose.words.loading/pdfloadoptions/skip_pdf_images/
---

## PdfLoadOptions.skip_pdf_images property

Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is ``False``.



### Examples

Shows how to skip images during loading PDF files.

```python
options = aw.loading.PdfLoadOptions()
options.skip_pdf_images = is_skip_pdf_images

doc = aw.Document(MY_DIR + "Images.pdf", options)
shape_collection = doc.get_child_nodes(aw.NodeType.SHAPE, True)

if is_skip_pdf_images:
    self.assertEqual(shape_collection.count, 0)
else:
    self.assertNotEqual(shape_collection.count, 0)
```

### See Also

* module [aspose.words.loading](../../)
* class [PdfLoadOptions](../)

