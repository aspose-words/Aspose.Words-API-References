---
title: "Aspose::Words::Fields::FieldAddressBlock 类"
linktitle: "FieldAddressBlock"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAddressBlock 类。实现 ADDRESSBLOCK 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class


实现 ADDRESSBLOCK 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldAddressBlock : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IFormattableMergeField
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FieldAddressBlock](./fieldaddressblock/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/)() | 获取或设置排除的国家/地区名称。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/)() | 获取或设置是否根据收件人所在国家/地区（由 POST*CODE（世界邮政联盟 2006）定义）来格式化地址。 |
| [get_IncludeCountryOrRegionName](./get_includecountryorregionname/)() | 获取或设置是否包含国家/地区名称。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LanguageId](./get_languageid/)() | 获取或设置用于格式化地址的语言 ID。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_NameAndAddressFormat](./get_nameandaddressformat/)() | 获取或设置名称和地址格式。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetFieldNames](./getfieldnames/)() override | 返回该字段使用的邮件合并字段名称的集合。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_ExcludedCountryOrRegionName](./set_excludedcountryorregionname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/) 的 setter。 |
| [set_FormatAddressOnCountryOrRegion](./set_formataddressoncountryorregion/)(bool) | 用于设置 [Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/) 的 setter。 |
| [set_IncludeCountryOrRegionName](./set_includecountryorregionname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAddressBlock::get_IncludeCountryOrRegionName](./get_includecountryorregionname/) 的 setter。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LanguageId](./set_languageid/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAddressBlock::get_LanguageId](./get_languageid/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_NameAndAddressFormat](./set_nameandaddressformat/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat](./get_nameandaddressformat/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
