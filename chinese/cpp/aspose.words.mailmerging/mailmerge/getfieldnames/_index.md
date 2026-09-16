---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNames 方法"
linktitle: "GetFieldNames"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNames 方法。返回文档中可用的邮件合并字段名称集合（C++）。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge::GetFieldNames method


返回文档中可用的邮件合并字段名称集合。

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNames()
```

## 备注


返回完整的合并字段名称，包括可选前缀。不消除重复的字段名称。

每次调用都会创建一个新的字符串数组。

如果 [UseNonMergeFields](../get_usenonmergefields/) 为 **true**，则包括 "mustache" 字段名称。
## 另见

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
