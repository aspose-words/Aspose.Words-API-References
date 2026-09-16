---
title: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions 方法"
linktitle: "ExecuteWithRegions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions 方法。使用自定义数据源和邮件合并区域在 C++ 中执行邮件合并。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


从自定义数据源并使用邮件合并区域执行邮件合并。

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 数据源 | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | 实现自定义邮件合并数据源接口的对象。 |
## 备注


使用此方法可将文档中的邮件合并字段填充为来自任何自定义数据源（如 XML 文件或业务对象集合）的值。您需要编写实现 [IMailMergeDataSource](../../imailmergedatasource/) 接口的自定义类。

仅当 [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) 为 **false** 时才能使用此方法，即您不需要从右到左语言（如阿拉伯语或希伯来语）的兼容性。

## 另见

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


从自定义数据源并使用邮件合并区域执行邮件合并。

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | 实现自定义邮件合并数据源根接口的对象。 |
## 备注


使用此方法可将文档中的邮件合并字段填充为来自任何自定义数据源（如 XML 文件或业务对象集合）的值。您需要编写实现 [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) 和 [IMailMergeDataSource](../../imailmergedatasource/) 接口的自定义类。

仅当 [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) 为 **false** 时才能使用此方法，即您不需要从右到左语言（如阿拉伯语或希伯来语）的兼容性。

## 另见

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
