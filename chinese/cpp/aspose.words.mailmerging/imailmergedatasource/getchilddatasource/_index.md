---
title: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource 方法"
linktitle: "GetChildDataSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource 方法。Aspose.Words 邮件合并引擎在 C++ 中遇到嵌套邮件合并区域的开始时调用此方法。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开始时调用此方法。

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| tableName | System::String | 模板文档中指定的邮件合并区域的名称。大小写不敏感。 |

### ReturnValue

一个数据源对象，可提供对指定表的数据记录的访问。
## 备注


当 Aspose.Words 邮件合并引擎用数据填充邮件合并区域并遇到形如 MERGEFIELD TableStart:TableName 的嵌套邮件合并区域的开始时，它会在当前数据源对象上调用 [GetChildDataSource()](./)。您的实现需要返回一个新的数据源对象，以提供对当前父记录的子记录的访问。Aspose.Words 将使用返回的数据源来填充嵌套的邮件合并区域。

以下是 [GetChildDataSource()](./) 实现必须遵循的规则。

如果此数据源对象所代表的表具有具有指定名称的相关子（明细）表，则您的实现需要返回一个新的 [IMailMergeDataSource](../) 对象，以提供对当前记录的子记录的访问。一个示例是 Orders / OrderDetails 关系。假设当前的 [IMailMergeDataSource](../) 对象表示 Orders 表，并且它有一个当前的订单记录。接下来，Aspose.Words 在文档中遇到 \"MERGEFIELD TableStart:OrderDetails\" 并调用 [GetChildDataSource()](./)。您需要创建并返回一个 [IMailMergeDataSource](../) 对象，以允许 Aspose.Words 访问当前订单的 OrderDetails 记录。

如果此数据源对象没有与指定名称的表的关联，则需要返回一个 [IMailMergeDataSource](../) 对象，以提供对指定表所有记录的访问。

如果不存在具有指定名称的表，您的实现应返回 **null**。

## 另见

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
