---
title: "Aspose::Words::MailMerging::FieldMergingArgsBase class"
linktitle: "FieldMergingArgsBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::FieldMergingArgsBase class. FieldMergingArgs 和 ImageFieldMergingArgs 的基类。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class


[FieldMergingArgs](../fieldmergingargs/) 和 [ImageFieldMergingArgs](../imagefieldmergingargs/) 的基类。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class FieldMergingArgsBase : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](./get_document/)() const | 返回执行邮件合并的 [Document](./get_document/) 对象。 |
| [get_DocumentFieldName](./get_documentfieldname/)() const | 获取文档中指定的合并字段名称。 |
| [get_Field](./get_field/)() const | 获取表示当前合并字段的对象。 |
| [get_FieldName](./get_fieldname/)() const | 获取数据源中合并字段的名称。 |
| [get_FieldValue](./get_fieldvalue/)() const | 获取来自数据源的字段值。 |
| [get_RecordIndex](./get_recordindex/)() const | 获取正在合并的记录的零基索引。 |
| [get_TableName](./get_tablename/)() const | 获取当前合并操作的数据表名称；如果名称不可用，则返回空字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](./set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | 设置来自数据源的字段值。 |
| static [Type](./type/)() |  |

## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
