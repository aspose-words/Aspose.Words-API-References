---
title: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion 方法"
linktitle: "GetFieldNamesForRegion"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion 方法。返回在 C++ 中可在该区域使用的邮件合并字段名称的集合。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## MailMerge::GetFieldNamesForRegion(const System::String\&) method


返回区域中可用的邮件合并字段名称集合。

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| regionName | const System::String\& | 区域名称（不区分大小写）。 |
## 备注


返回完整的合并字段名称，包括可选前缀。不消除重复的字段名称。

如果文档包含多个同名区域，则处理第一个区域。

每次调用都会创建一个新的字符串数组。

## 另见

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::GetFieldNamesForRegion(const System::String\&, int32_t) method


返回区域中可用的邮件合并字段名称集合。

```cpp
System::ArrayPtr<System::String> Aspose::Words::MailMerging::MailMerge::GetFieldNamesForRegion(const System::String &regionName, int32_t regionIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| regionName | const System::String\& | 区域名称（不区分大小写）。 |
| regionIndex | int32_t | 区域索引（从零开始）。 |
## 备注


返回完整的合并字段名称，包括可选前缀。不消除重复的字段名称。

如果文档包含多个同名区域，则处理第 N 个区域（从零开始）。

每次调用都会创建一个新的字符串数组。

## 另见

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
