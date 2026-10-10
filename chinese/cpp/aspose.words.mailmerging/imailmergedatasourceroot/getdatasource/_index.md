---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource 方法"
linktitle: "GetDataSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource 方法。当 Aspose.Words 邮件合并引擎在 C++ 中遇到顶层邮件合并区域的开始时，会调用此方法。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Aspose.Words 邮件合并引擎在遇到顶级邮件合并区域的开始时调用此方法。

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| tableName | System::String | 模板文档中指定的邮件合并区域的名称。大小写不敏感。 |

### ReturnValue

一个数据源对象，可提供对指定表的数据记录的访问。
## 备注


当 Aspose.Words 邮件合并引擎用数据填充文档并遇到 MERGEFIELD TableStart:TableName 时，它会在此对象上调用 [GetDataSource()](./)。您的实现需要返回一个新的数据源对象。Aspose.Words 将使用返回的数据源来填充邮件合并区域。

如果不存在具有指定名称的数据源（表），您的实现应返回 **null**。

## 另见

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
