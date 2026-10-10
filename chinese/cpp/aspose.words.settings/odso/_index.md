---
title: "Aspose::Words::Settings::Odso 类"
linktitle: "Odso"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::Odso 类。指定用于邮件合并数据源的 Office 数据源对象 (ODSO) 设置。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.settings/odso/
---
## Odso class


指定邮件合并数据源的 Office 数据源对象 (ODSO) 设置。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class Odso : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 返回此对象的深度克隆。 |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | 指定应被解释为用于分隔外部数据源中列的列分隔符字符。默认值为 0，表示未定义列分隔符。 |
| [get_DataSource](./get_datasource/)() const | 指定用于连接文档以执行邮件合并的外部数据源的位置。默认值为空字符串。 |
| [get_DataSourceType](./get_datasourcetype/)() const | 指定作为此邮件合并的 ODSO 连接信息的一部分要连接的外部数据源类型。默认值为 [Default](../odsodatasourcetype/)。 |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | 获取一组对象，这些对象指定外部数据源的列如何映射到文档中预定义的合并字段名称。此对象永不为 **null**。 |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | 指定宿主应用程序应将指定外部数据源中的第一行数据视为包含数据源中每列名称的标题行。默认值为 **false**。 |
| [get_RecipientDatas](./get_recipientdatas/)() const | 获取一组对象，这些对象指定邮件合并中各个记录的包含/排除。此对象永不为 **null**。 |
| [get_TableName](./get_tablename/)() const | 指定源在外部数据源中应连接的特定数据集。默认值为空字符串。 |
| [get_UdlConnectString](./get_udlconnectstring/)() const | 指定用于连接外部数据源的通用数据链接 (UDL) 连接字符串。默认值为空字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | 用于 [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/) 的设置器。 |
| [set_DataSource](./set_datasource/)(const System::String\&) | 指定用于连接文档以执行邮件合并的外部数据源的位置。默认值为空字符串。 |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | 用于 [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/) 的设置器。 |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | 设置一组对象，这些对象指定外部数据源的列如何映射到文档中预定义的合并字段名称。此对象永不为 **null**。 |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | 用于 [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/) 的设置器。 |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | 设置一组对象，这些对象指定邮件合并中各个记录的包含/排除。此对象永不为 **null**。 |
| [set_TableName](./set_tablename/)(const System::String\&) | 指定源在外部数据源中应连接的特定数据集。默认值为空字符串。 |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | 指定用于连接外部数据源的通用数据链接 (UDL) 连接字符串。默认值为空字符串。 |
| static [Type](./type/)() |  |
## 备注


ODSO 似乎是较新 Microsoft Word 版本在为邮件合并文档指定某些类型的数据源时更倾向使用的“新”方式。ODSO 可能首次出现在 Microsoft Word 2000 中。

ODSO 的使用文档很少，学习如何使用此对象的属性的最佳方法是先在 Microsoft Word 中手动创建一个带有所需数据源的文档，然后使用 Aspose.Words 打开该文档并检查 [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) 和 [Odso](../mailmergesettings/get_odso/) 对象的属性。例如，这是一种学习如何以编程方式配置数据源的好方法。

通常不需要直接创建此类的对象，因为 ODSO 设置始终可通过 [Odso](../mailmergesettings/get_odso/) 属性获取。

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
