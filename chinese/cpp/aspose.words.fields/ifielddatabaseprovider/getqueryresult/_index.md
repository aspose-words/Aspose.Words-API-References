---
title: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult 方法"
linktitle: "GetQueryResult"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult 方法. 返回 C++ 中的查询结果。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


返回查询结果。

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | System::String | 在 \d 字段开关中指定的数据库的完整路径和文件名。 |
| 连接 | System::String | 在 \c 字段开关中指定的数据的连接。 |
| 查询 | System::String | 在 \s 字段开关中指定的数据库的 SQL 指令集合。 |
| 字段 | System::SharedPtr\<Aspose::Words::Fields::FieldDatabase\> | 正在更新的字段。 |

### ReturnValue

用于字段更新的 [FieldDatabaseDataTable](../../fielddatabasedatatable/) 实例。

## 另见

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
