---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /zh/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(file_name=MY_DIR + 'Unoptimized document.docx')
# 创建一个 "XpsSaveOptions" 对象，以传递给文档的 "Save" 方法
# 以修改该方法将文档转换为 .XPS 的方式。
save_options = aw.saving.XpsSaveOptions()
# 将 "OptimizeOutput" 属性设置为 "true"，以采取诸如删除嵌套或空白画布等措施
# 并将相邻具有相同格式的运行合并，以优化输出文档的内容。
# 这可能会影响文档的外观。
# 将 "OptimizeOutput" 属性设置为 "false"，以正常保存文档。
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

