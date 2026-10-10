---
title: "Aspose::Words::Settings::OdsoRecipientData 类"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::OdsoRecipientData 类。表示有关外部数据源中单个记录的信息，该记录将在邮件合并时被排除。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


表示外部数据源中单个记录的信息，该记录将从邮件合并中排除。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class OdsoRecipientData : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 返回此对象的深度克隆。 |
| [get_Active](./get_active/)() const | 指定在执行邮件合并时，是否应将来自数据源的记录导入文档。默认值为 **true**。 |
| [get_Column](./get_column/)() const | 指定数据源中包含当前记录唯一数据的列。默认值为 0。 |
| [get_Hash](./get_hash/)() const | 表示此记录的哈希码。有时 Microsoft Word 使用整个记录的 [Hash](./get_hash/) 而不是 [UniqueTag](./get_uniquetag/) 值。默认值为 0。 |
| [get_UniqueTag](./get_uniquetag/)() const | 指定在包含唯一数据的列中给定记录的内容。默认值为 **null**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | 指定在执行邮件合并时，是否应将来自数据源的记录导入文档。默认值为 **true**。 |
| [set_Column](./set_column/)(int32_t) | 指定数据源中包含当前记录唯一数据的列。默认值为 0。 |
| [set_Hash](./set_hash/)(int32_t) | 表示此记录的哈希码。有时 Microsoft Word 使用整个记录的 [Hash](./get_hash/) 而不是 [UniqueTag](./get_uniquetag/) 值。默认值为 0。 |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | 指定在包含唯一数据的列中给定记录的内容。默认值为 **null**。 |
| static [Type](./type/)() |  |
## 备注


如果记录应合并到合并文档中，则无需该记录的任何信息。但是，如果给定记录不应合并到合并文档中，则该记录的唯一键值应存储在此对象的 [UniqueTag](./get_uniquetag/) 属性中，以指示此排除。
## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
