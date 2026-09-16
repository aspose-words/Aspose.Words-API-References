---
title: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields 方法"
linktitle: "get_UseNonMergeFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields 方法。当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并还会在 C++ 中对其他类型的字段以及 \"{{fieldName}}\" 标记执行。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


当 **true** 时，指定除了 MERGEFIELD 字段之外，邮件合并还会执行到其他类型的字段以及 \"{{fieldName}}\" 标签中。

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## 备注


通常，邮件合并仅针对 MERGEFIELD 字段执行，但一些客户的报表是使用其他字段构建的，并且因此产生了大量此类文档。为了简化迁移（并且因为该方法已被多个客户独立使用），引入了对其他字段进行邮件合并的功能。

当 [UseNonMergeFields](./) 设置为 **true** 时，Aspose.Words 将对以下字段执行邮件合并：

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

此外，当 [UseNonMergeFields](./) 设置为 **true** 时，Aspose.Words 将对文本标签 "{{fieldName}}" 执行邮件合并。这些不是字段，而只是文本标签。
## 另见

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
