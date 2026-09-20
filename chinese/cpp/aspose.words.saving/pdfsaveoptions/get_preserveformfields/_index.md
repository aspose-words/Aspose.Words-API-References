---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields 方法"
linktitle: "get_PreserveFormFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields 方法。指定是将 Microsoft Word 表单字段保留为 PDF 中的表单字段还是转换为文本。默认在 C++ 中为 false。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


指定是将 Microsoft Word 表单字段保留为 PDF 中的表单字段还是将其转换为文本。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## 备注


Microsoft Word 表单字段包括文本输入、下拉列表和复选框控件。

当设置为 **false** 时，这些字段将以文本形式导出到 PDF。设置为 **true** 时，这些字段将导出为 PDF 表单字段。

将表单字段导出为 PDF 表单字段时，可能会出现一些格式丢失，因为 PDF 表单字段不支持 Microsoft Word 表单字段的所有功能。

此外，输出大小取决于内容大小，因为 Microsoft Word 中的可编辑表单是内联对象。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
