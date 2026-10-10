---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts 方法"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts 方法。指定是否在 PDF 中生成模拟特定 Microsoft Word 表单字段行为的脚本。默认在 C++ 中为 false。"
type: docs
weight: 18500
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


指定是否在 PDF 中生成模拟特定 Microsoft Word 表单字段行为的脚本。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## 备注


启用此选项后，导出器会生成 PDF JavaScript 动作，以模拟 Microsoft Word 表单字段行为，例如具有格式和验证规则的日期和时间表单字段。

设置为 **true** 时，支持的行为将导出为 PDF JavaScript 动作。设置为 **false** 时，将不生成表单字段脚本。

脚本执行取决于 PDF 查看器。某些 PDF 查看器可能会忽略脚本、限制脚本执行，或要求用户启用 JavaScript。

PDF/A-1、PDF/A-2 和 PDF/A-3 合规性禁止 JavaScript 动作。在这种情况下将自动使用 **false** 值。
## 另见

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
