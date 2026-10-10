---
title: "Aspose::Words::Settings::MailMergeSettings class"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::MailMergeSettings class. 指定文档的所有邮件合并信息。要了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


指定文档的所有邮件合并信息。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class MailMergeSettings : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clear](./clear/)() | 以一种方式清除邮件合并设置，使得文档保存时不会保存任何邮件合并设置，文档将成为普通文档。 |
| [Clone](./clone/)() | 返回此对象的深度克隆。 |
| [get_ActiveRecord](./get_activerecord/)() const | 指定来自数据源的记录在 Microsoft Word 中显示的基于 1 的索引。默认值为 1。 |
| [get_AddressFieldName](./get_addressfieldname/)() const | 指定数据源中包含电子邮件地址的列。默认值为空字符串。 |
| [get_CheckErrors](./get_checkerrors/)() const | 指定 Microsoft Word 在执行邮件合并时进行的错误报告类型。默认值为 [Default](../mailmergecheckerrors/)。 |
| [get_ConnectString](./get_connectstring/)() const | 指定用于连接外部数据源的连接字符串。默认值为空字符串。 |
| [get_DataSource](./get_datasource/)() const | 指定邮件合并数据源的路径。默认值为空字符串。 |
| [get_DataType](./get_datatype/)() const | 指定邮件合并数据源的类型以及数据访问方式。默认值为 [Default](../mailmergedatatype/)。 |
| [get_Destination](./get_destination/)() const | 指定 Microsoft Word 将如何输出邮件合并的结果。默认值为 [Default](../mailmergedestination/)。 |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | 指定执行邮件合并的应用程序应如何处理合并文档中由邮件合并产生的空行。默认值为 **false**。 |
| [get_HeaderSource](./get_headersource/)() const | 指定邮件合并标题源的路径。默认值为空字符串。 |
| [get_LinkToQuery](./get_linktoquery/)() const | 对此不确定。Microsoft Word 自动化参考指出，这指定每次在 Microsoft Word 中打开文档时都会执行查询。但 OOXML 规范指出，这指定查询包含对外部查询文件的引用，该文件包含实际查询。默认值为 **false**。 |
| [get_MailAsAttachment](./get_mailasattachment/)() const | 指定在邮件合并操作期间生成的文档应作为附件发送，而不是作为实际电子邮件的正文。默认值为 **false**。 |
| [get_MailSubject](./get_mailsubject/)() const | 指定在邮件合并期间生成的电子邮件或传真主题行中出现的文本。默认值为空字符串。 |
| [get_MainDocumentType](./get_maindocumenttype/)() const | 指定邮件合并主文档类型。默认值为 [Default](../mailmergemaindocumenttype/)。 |
| [get_Odso](./get_odso/)() const | 获取指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [get_Query](./get_query/)() const | 包含将在指定的外部数据源上运行的结构化查询语言 (SQL) 字符串，以返回在执行邮件合并操作时将导入文档的记录集。默认值为空字符串。 |
| [get_ViewMergedData](./get_viewmergeddata/)() const | 指定 Microsoft Word 应显示已插入合并字段的指定外部数据源中的数据（例如预览合并数据）。默认值为 **false**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | 指定来自数据源的记录在 Microsoft Word 中显示的基于 1 的索引。默认值为 1。 |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | 指定数据源中包含电子邮件地址的列。默认值为空字符串。 |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | 指定 Microsoft Word 在执行邮件合并时进行的错误报告类型。默认值为 [Default](../mailmergecheckerrors/)。 |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | 指定用于连接外部数据源的连接字符串。默认值为空字符串。 |
| [set_DataSource](./set_datasource/)(const System::String\&) | 指定邮件合并数据源的路径。默认值为空字符串。 |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | 指定邮件合并数据源的类型以及数据访问方式。默认值为 [Default](../mailmergedatatype/)。 |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | 指定 Microsoft Word 将如何输出邮件合并的结果。默认值为 [Default](../mailmergedestination/)。 |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | 指定执行邮件合并的应用程序应如何处理合并文档中由邮件合并产生的空行。默认值为 **false**。 |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | 指定邮件合并标题源的路径。默认值为空字符串。 |
| [set_LinkToQuery](./set_linktoquery/)(bool) | 用于设置 [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/) 的 setter。 |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | 指定在邮件合并操作期间生成的文档应作为附件发送，而不是作为实际电子邮件的正文。默认值为 **false**。 |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | 指定在邮件合并期间生成的电子邮件或传真主题行中出现的文本。默认值为空字符串。 |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | 用于设置 [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/) 的 setter。 |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | 设置指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [set_Query](./set_query/)(const System::String\&) | 包含将在指定的外部数据源上运行的结构化查询语言 (SQL) 字符串，以返回在执行邮件合并操作时将导入文档的记录集。默认值为空字符串。 |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | 指定 Microsoft Word 应显示已插入合并字段的指定外部数据源中的数据（例如预览合并数据）。默认值为 **false**。 |
| static [Type](./type/)() |  |
## 备注


您可以使用此对象为文档指定邮件合并数据源，且该信息（以及可用的数据字段）将在用户打开此文档时出现在 Microsoft Word 中。或者，您可以使用此对象查询用户在 Microsoft Word 为此文档指定的邮件合并设置。

通常不需要直接创建此类的对象，因为文档的邮件合并设置始终可通过 [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) 属性获取。

要检测此文档是否为邮件合并主文档，请检查 [MainDocumentType](./get_maindocumenttype/) 属性的值。

要从文档中移除邮件合并设置和数据源信息，您可以使用 [Clear](./clear/) 方法。如果 [MainDocumentType](./get_maindocumenttype/) 属性设置为 [NotAMergeDocument](../mailmergemaindocumenttype/) 或 [DataType](./get_datatype/) 属性设置为 [None](../mailmergedatatype/)，Aspose.Words 将不会将邮件合并设置写入文档。

学习如何使用此对象属性的最佳方法是先在 Microsoft Word 中手动创建一个带有所需数据源的文档，然后使用 Aspose.Words 打开该文档并检查 [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) 和 [Odso](./get_odso/) 对象的属性。如果您想了解如何以编程方式配置数据源，这是一种不错的做法。

Aspose.Words 在加载、保存和在不同格式之间转换文档时会保留邮件合并信息，但在使用 [MailMerge](../../aspose.words.mailmerging/mailmerge/) 对象执行自身的邮件合并时不会使用这些信息。

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
