---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName 方法"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName 方法。指定在 C++ 中是否使用 SDT 控件的 Tag 或 Id 属性作为 PDF 表单字段的名称。"
type: docs
weight: 32500
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


指定是否在 PDF 中使用 SDT 控件的 Tag 或 Id 属性作为表单字段的名称。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## 备注


默认值为 **false**。

设置为 **false** 时，SDT 控件的 Id 属性用作 PDF 表单字段的名称。

设置为 **true** 时，SDT 控件的 Tag 属性用作 PDF 表单字段的名称。

如果设置为 **true** 且 Tag 为空，则使用 Id 属性作为表单字段名称。

如果设置为 **true** 且 Tag 值不唯一，重复的 Tag 值将被修改以生成唯一的 PDF 表单字段名称。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
