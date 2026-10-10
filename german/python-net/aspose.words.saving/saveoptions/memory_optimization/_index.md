---
title: SaveOptions.memory_optimization property
linktitle: memory_optimization property
articleTitle: memory_optimization property
second_title: Aspose.Words for Python
description: "SaveOptions.memory_optimization property. Gets or sets value determining if memory optimization should be performed before saving the document"
type: docs
weight: 80
url: /de/python-net/aspose.words.saving/saveoptions/memory_optimization/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.SaveOptions.create_save_options(save_format=aw.SaveFormat.PDF)
# Setzen Sie die Eigenschaft \"MemoryOptimization\" auf \"true\", um den Speicherverbrauch bei den Speicheroperationen großer Dokumente zu reduzieren
# auf Kosten einer längeren Dauer des Vorgangs.
# Setzen Sie die Eigenschaft \"MemoryOptimization\" auf \"false\", um das Dokument normal als PDF zu speichern.
save_options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.MemoryOptimization.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

