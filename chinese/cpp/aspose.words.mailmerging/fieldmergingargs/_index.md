---
title: "Aspose::Words::MailMerging::FieldMergingArgs 类"
linktitle: "FieldMergingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::FieldMergingArgs 类。提供 MergeField 事件的数据。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


为 **MergeField** 事件提供数据。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | 返回用于执行邮件合并的 [Document](../fieldmergingargsbase/get_document/) 对象。 |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | 获取文档中指定的合并字段名称。 |
| [get_Field](../fieldmergingargsbase/get_field/)() const | 获取表示当前合并字段的对象。 |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | 获取数据源中合并字段的名称。 |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | 获取来自数据源的字段值。 |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | 获取正在合并的记录的零基索引。 |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | 获取当前合并操作的数据表名称；如果名称不可用，则返回空字符串。 |
| [get_Text](./get_text/)() const | 获取或设置将在文档中为当前合并字段插入的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | 设置来自数据源的字段值。 |
| [set_Text](./set_text/)(const System::String\&) | 用于 [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


当文档中遇到简单的邮件合并字段时，**MergeField** 事件在邮件合并期间触发。您可以响应此事件以返回文本，供邮件合并引擎插入到文档中。

## 另见

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
