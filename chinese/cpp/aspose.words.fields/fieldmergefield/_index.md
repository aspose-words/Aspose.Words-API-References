---
title: "Aspose::Words::Fields::FieldMergeField 类"
linktitle: "FieldMergeField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldMergeField 类。实现 MERGEFIELD 字段。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 67000
url: /zh/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


实现 MERGEFIELD 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldName](./get_fieldname/)() | 获取数据字段的名称。 |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | 仅返回数据字段的名称。任何前缀都会被剥离到 prefix 属性。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_IsMapped](./get_ismapped/)() | 获取此字段是否为映射字段。 |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | 获取是否启用垂直格式的字符转换。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_TextAfter](./get_textafter/)() | 获取在字段非空时要插入在字段之后的文本。 |
| [get_TextBefore](./get_textbefore/)() | 获取在字段非空时要插入在字段之前的文本。 |
| [get_Type](./get_type/)() const override | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_FieldName](./set_fieldname/)(const System::String\&) | 设置数据字段的名称。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_IsMapped](./set_ismapped/)(bool) | 设置此字段是否为映射字段。 |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | 设置是否启用垂直格式的字符转换。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_TextAfter](./set_textafter/)(const System::String\&) | 设置在字段非空时要插入在字段之后的文本。 |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | 设置在字段非空时要插入在字段之前的文本。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
