---
title: SaveOptions.create_save_options method
linktitle: create_save_options method
articleTitle: create_save_options method
second_title: Aspose.Words for Python
description: "aspose.words.saving.SaveOptions.create_save_options method"
type: docs
weight: 210
url: /zh/python-net/aspose.words.saving/saveoptions/create_save_options/
---

## create_save_options(save_format) {#saveformat}

Creates a save options object of a class suitable for the specified save format.


```python
def create_save_options(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | The save format for which to create a save options object. |

### Returns

An object of a class that derives from [SaveOptions](../).


## create_save_options(file_name) {#str}

Creates a save options object of a class suitable for the file extension specified in the given file name.


```python
def create_save_options(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The extension of this file name determines the class of the save options object to create. |

### Returns

An object of a class that derives from [SaveOptions](../).


## Examples

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

Shows how to set a default template for documents that do not have attached templates.

```python
doc = aw.Document()
# 启用自动样式更新，但不要附加模板文档。
doc.automatically_update_styles = True
self.assertEqual('', doc.attached_template)
# 由于没有模板文档，文档没有地方跟踪样式更改。
# 使用 SaveOptions 对象自动设置模板
# 如果我们正在保存的文档没有模板的话。
options = aw.saving.SaveOptions.create_save_options(file_name='Document.DefaultTemplate.docx')
options.default_template = MY_DIR + 'Business brochure.dotx'
doc.save(file_name=ARTIFACTS_DIR + 'Document.DefaultTemplate.docx', save_options=options)
```

## See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

