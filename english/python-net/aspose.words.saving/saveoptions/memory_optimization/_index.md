---
title: SaveOptions.memory_optimization property
linktitle: memory_optimization property
articleTitle: memory_optimization property
second_title: Aspose.Words for Python
description: "SaveOptions.memory_optimization property. Gets or sets value determining if memory optimization should be performed before saving the document"
type: docs
weight: 80
url: /python-net/aspose.words.saving/saveoptions/memory_optimization/
---

## SaveOptions.memory_optimization property

Gets or sets value determining if memory optimization should be performed before saving the document.
Default value for this property is ``False``.



```python
@property
def memory_optimization(self) -> bool:
    ...

@memory_optimization.setter
def memory_optimization(self, value: bool):
    ...

```

### Remarks

Setting this option to ``True`` can significantly decrease memory consumption while saving large documents at the cost of slower saving time.



### Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.SaveOptions.create_save_options(aw.SaveFormat.PDF)
# Set the "memory_optimization" property to "True" to lower the memory footprint of large documents' saving operations
# at the cost of increasing the duration of the operation.
# Set the "memory_optimization" property to "False" to save the document as a PDF normally.
save_options.memory_optimization = memory_optimization
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.memory_optimization.pdf', save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

