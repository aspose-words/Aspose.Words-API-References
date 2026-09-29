---
title: SaveOptions.memory_optimization property
linktitle: memory_optimization property
articleTitle: memory_optimization property
second_title: Aspose.Words for Python
description: "SaveOptions.memory_optimization property. Gets or sets value determining if memory optimization should be performed before saving the document"
type: docs
weight: 80
url: /es/python-net/aspose.words.saving/saveoptions/memory_optimization/
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
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
save_options = aw.saving.SaveOptions.create_save_options(save_format=aw.SaveFormat.PDF)
# Establezca la propiedad "MemoryOptimization" en "true" para reducir la huella de memoria de las operaciones de guardado de documentos grandes
# a costa de aumentar la duración de la operación.
# Establezca la propiedad "MemoryOptimization" en "false" para guardar el documento como PDF normalmente.
save_options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.MemoryOptimization.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

