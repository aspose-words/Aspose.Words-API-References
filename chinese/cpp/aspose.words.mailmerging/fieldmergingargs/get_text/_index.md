---
title: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::FieldMergingArgs::get_Text 方法。获取或设置将在 C++ 中为当前合并字段插入到文档的文本。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


获取或设置将在文档中为当前合并字段插入的文本。

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## 备注


当调用您的事件处理程序时，此属性被设置为 **null**。

如果将 Text 保持为 **null**，邮件合并引擎将在合并字段的位置插入 [FieldValue](../../fieldmergingargsbase/get_fieldvalue/)。

如果将 Text 设置为任意字符串（包括空字符串），该字符串将在合并字段的位置插入到文档中。
## 另见

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
