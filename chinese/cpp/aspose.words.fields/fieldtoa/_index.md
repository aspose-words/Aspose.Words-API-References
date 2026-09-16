---
title: "Aspose::Words::Fields::FieldToa 类"
linktitle: "FieldToa"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldToa 类。实现 TOA 字段。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 104000
url: /zh/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


实现 TOA 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | 获取标记用于构建表格的文档部分的书签名称。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_EntryCategory](./get_entrycategory/)() | 获取表格中条目的整体类别。 |
| [get_EntrySeparator](./get_entryseparator/)() | 获取用于分隔权威表条目及其页码的字符序列。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | 获取用于在页码列表中分隔两个页码的字符序列。 |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | 获取用于分隔页码范围起止的字符序列。 |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | 获取是否从权威表条目中删除文档中条目文本的格式。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SequenceName](./get_sequencename/)() | 获取与页码一起包含编号的序列的名称。 |
| [get_SequenceSeparator](./get_sequenceseparator/)() | 获取用于分隔序列号和页码的字符序列。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_UseHeading](./get_useheading/)() | 获取是否在权威表条目中包含类别标题。 |
| [get_UsePassim](./get_usepassim/)() | 获取是否将同一权威的五个或更多不同页码引用替换为 "passim"，该词用于指示在被引用作品中某个词或段落频繁出现。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 设置标记用于构建表格的文档部分的书签名称。 |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | 设置包含在表格中的条目的整体类别。 |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | 设置用于分隔权威表条目及其页码的字符序列。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | 设置用于在页码列表中分隔两个页码的字符序列。 |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | 设置用于分隔页码范围起止的字符序列。 |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | 设置是否从权威表条目中删除文档中条目文本的格式。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | 设置与页码一起包含编号的序列的名称。 |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | 设置用于分隔序列号和页码的字符序列。 |
| [set_UseHeading](./set_useheading/)(bool) | 设置是否在权威表条目中包含类别标题。 |
| [set_UsePassim](./set_usepassim/)(bool) | 设置是否将同一权威的五个或更多不同页码引用替换为 "passim"，该词用于指示在被引用作品中某个词或段落频繁出现。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
