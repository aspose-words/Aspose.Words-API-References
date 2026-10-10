---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. 指定作为 C++ 中 ODSO 连接信息的一部分要连接的外部数据源的类型。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


指定作为 ODSO 连接信息一部分要连接的外部数据源的类型。

```cpp
enum class OdsoDataSourceType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 文本 | 0 | 指定给定文档已连接到文本文件。可能是 wdMergeSubTypeOther。 |
| 数据库 | 1 | 指定给定文档已连接到数据库。可能是 wdMergeSubTypeAccess。 |
| AddressBook | 2 | 指定给定文档已连接到联系人地址簿。可能是 wdMergeSubTypeOAL。 |
| Document1 | 3 | 指定给定文档已连接到由生成应用程序支持的另一种文档格式。可能是 wdMergeSubTypeOLEDBWord。 |
| Document2 | 4 | 指定给定文档已连接到由生成应用程序支持的另一种文档格式。可能是 wdMergeSubTypeWorks。 |
| Native | 5 | 指定给定文档已连接到生成应用程序本机的另一种文档格式。可能是 wdMergeSubTypeOLEDBText。 |
| Email | 6 | 指定给定文档已连接到电子邮件应用程序。可能是 wdMergeSubTypeOutlook。 |
| None | 7 | 未指定外部数据源的类型。可能是 wdMergeSubTypeWord。 |
| 旧版 | 8 | 指定给定文档已连接到由生成应用程序支持的旧版文档格式。可能是 wdMergeSubTypeWord2000。 |
| 母版 | 9 | 指定给定文档已连接到一个聚合其他数据源的数据源。 |
| Default | n/a | 等于 [None](./)。 |

## 备注


OOXML 规范对该枚举描述非常模糊。我猜它可能对应于 WdMergeSubType 枚举 [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx)。

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
