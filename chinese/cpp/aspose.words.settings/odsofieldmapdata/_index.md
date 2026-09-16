---
title: "Aspose::Words::Settings::OdsoFieldMapData 类"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::OdsoFieldMapData 类。指定外部数据源中的列如何映射到文档内的预定义合并字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


指定外部数据源中的列如何映射到文档内预定义的合并字段。欲了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class OdsoFieldMapData : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 返回此对象的深度克隆。 |
| [get_Column](./get_column/)() const | 指定外部数据源中列的零基索引，该列将映射到特定 MERGEFIELD 字段的本地名称。默认值为 0。 |
| [get_MappedName](./get_mappedname/)() const | 指定预定义的合并字段名称，该名称将映射到此字段映射中由 [Column](./get_column/) 属性指定的列号。默认值为空字符串。 |
| [get_Name](./get_name/)() const | 指定外部数据源中列的名称，该列的索引由 [Column](./get_column/) 属性指定。默认值为空字符串。 |
| [get_Type](./get_type/)() const | 指定给定的邮件合并字段是否已映射到给定外部数据源中的列。默认值为 [Default](../odsofieldmappingtype/)。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | 指定外部数据源中列的零基索引，该列将映射到特定 MERGEFIELD 字段的本地名称。默认值为 0。 |
| [set_MappedName](./set_mappedname/)(const System::String\&) | 指定预定义的合并字段名称，该名称将映射到此字段映射中由 [Column](./get_column/) 属性指定的列号。默认值为空字符串。 |
| [set_Name](./set_name/)(const System::String\&) | 指定外部数据源中列的名称，该列的索引由 [Column](./get_column/) 属性指定。默认值为空字符串。 |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | 指定给定的邮件合并字段是否已映射到给定外部数据源中的列。默认值为 [Default](../odsofieldmappingtype/)。 |
| static [Type](./type/)() |  |
## 备注


Microsoft Word 提供了一些预定义的合并字段名称，可将其插入文档作为 MERGEFIELD，或在 ADDRESSBLOCK 或 GREETINGLINE 字段中使用。[OdsoFieldMapData](./) 中指定的信息允许将外部数据源中的一列映射到单个预定义合并字段。

## 另见

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
