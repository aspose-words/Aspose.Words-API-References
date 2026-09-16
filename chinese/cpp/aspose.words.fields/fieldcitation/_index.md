---
title: "Aspose::Words::Fields::FieldCitation class"
linktitle: "FieldCitation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCitation class. 实现 CITATION 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


实现 CITATION 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | 获取与另一个源的 **Tag** 元素值匹配的值，以包含在引用中。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_FormatLanguageId](./get_formatlanguageid/)() | 获取用于配合指定书目样式在文档中格式化引用的语言 ID。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PageNumber](./get_pagenumber/)() | 获取与引用关联的页码。 |
| [get_Prefix](./get_prefix/)() | 获取添加到引用前面的前缀。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SourceTag](./get_sourcetag/)() | 获取与要插入的源的 **Tag** 元素值匹配的值。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_Suffix](./get_suffix/)() | 获取添加到引用后面的后缀。 |
| [get_SuppressAuthor](./get_suppressauthor/)() | 获取是否在引用中抑制作者信息。 |
| [get_SuppressTitle](./get_suppresstitle/)() | 获取是否在引用中抑制标题信息。 |
| [get_SuppressYear](./get_suppressyear/)() | 获取是否在引用中抑制年份信息。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_VolumeNumber](./get_volumenumber/)() | 获取与引用关联的卷号。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | 设置一个值，使其匹配另一个来源的 **Tag** 元素的值，以便包含在引用中。 |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | 设置语言 ID，该 ID 与指定的参考文献样式一起用于在文档中格式化引用。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | 设置与引用关联的页码。 |
| [set_Prefix](./set_prefix/)(const System::String\&) | 设置添加到引用前面的前缀。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | 设置一个值，使其匹配要插入的来源的 **Tag** 元素的值。 |
| [set_Suffix](./set_suffix/)(const System::String\&) | 设置添加到引用后面的后缀。 |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | 设置是否在引用中抑制作者信息。 |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | 设置是否在引用中抑制标题信息。 |
| [set_SuppressYear](./set_suppressyear/)(bool) | 设置是否在引用中抑制年份信息。 |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | 设置与引用关联的卷号。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
