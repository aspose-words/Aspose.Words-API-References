---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName 方法"
linktitle: "get_DocumentFieldName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName 方法。获取在文档中指定的合并字段的名称（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


获取文档中指定的合并字段名称。

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## 备注


如果您有一个将文档字段名映射到不同数据源字段名的映射，那么这就是文档中指定的原始字段名。

如果您在文档中指定了字段名前缀，例如 "Image:MyFieldName"，则 [DocumentFieldName](./) 返回不带前缀的字段名，即 "MyFieldName"。
## 另见

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
