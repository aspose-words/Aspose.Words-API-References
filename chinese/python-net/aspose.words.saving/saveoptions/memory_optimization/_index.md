---
title: SaveOptions.memory_optimization property
linktitle: memory_optimization property
articleTitle: memory_optimization property
second_title: Aspose.Words for Python
description: "SaveOptions.memory_optimization property. Gets or sets value determining if memory optimization should be performed before saving the document"
type: docs
weight: 80
url: /zh/python-net/aspose.words.saving/saveoptions/memory_optimization/
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
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.SaveOptions.create_save_options(save_format=aw.SaveFormat.PDF)
# 将 "MemoryOptimization" 属性设置为 "true" 以降低大型文档保存操作的内存占用
# 但会导致操作时间延长。
# 将 "MemoryOptimization" 属性设置为 "false" 以正常将文档保存为 PDF。
save_options.memory_optimization = memory_optimization
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.MemoryOptimization.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

