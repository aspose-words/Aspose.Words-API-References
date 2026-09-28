---
title: PdfSaveOptions.additional_text_positioning property
linktitle: additional_text_positioning property
articleTitle: additional_text_positioning property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.additional_text_positioning property. A flag specifying whether to write additional text positioning operators or not."
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/additional_text_positioning/
---

## PdfSaveOptions.additional_text_positioning property

A flag specifying whether to write additional text positioning operators or not.


```python
@property
def additional_text_positioning(self) -> bool:
    ...

@additional_text_positioning.setter
def additional_text_positioning(self, value: bool):
    ...

```

### Remarks

If ``True``, additional text positioning operators are written to the output PDF. This may help to overcome
issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.


The default value is ``False``.




### Examples

Show how to write additional text positioning operators.

```python
doc = aw.Document(file_name=MY_DIR + 'Text positioning operators.docx')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
save_options.text_compression = aw.saving.PdfTextCompression.NONE
# 将 "AdditionalTextPositioning" 属性设置为 "true"，尝试修复不正确的
# 输出 PDF 中的元素定位（如果有的话），代价是文件大小增加。
# 将 "AdditionalTextPositioning" 属性设置为 "false"，正常渲染文档。
save_options.additional_text_positioning = apply_additional_text_positioning
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.AdditionalTextPositioning.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

