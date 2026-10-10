---
title: "Aspose::Words::Fields::FieldDatabase 类"
linktitle: "FieldDatabase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldDatabase 类。实现 DATABASE 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


实现 DATABASE 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | 获取到数据的连接。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_FileName](./get_filename/)() | 获取数据库的完整路径和文件名。 |
| [get_FirstRecord](./get_firstrecord/)() | 获取要插入的第一条数据记录的整数记录号。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_FormatAttributes](./get_formatattributes/)() | 获取要应用于表格的格式属性。 |
| [get_InsertHeadings](./get_insertheadings/)() | 获取是否将来自数据库的字段名称插入为结果表中的列标题。 |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | 获取是否在合并开始时插入数据。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LastRecord](./get_lastrecord/)() | 获取要插入的最后一条数据记录的整数记录号。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Query](./get_query/)() | 获取查询数据库的 SQL 指令集合。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_TableFormat](./get_tableformat/)() | 获取要应用于数据库查询结果的格式。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_Connection](./set_connection/)(const System::String\&) | 设置数据的连接。 |
| [set_FileName](./set_filename/)(const System::String\&) | 设置数据库的完整路径和文件名。 |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | 设置要插入的第一条数据记录的整数记录号。 |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | 设置要应用于表格的格式属性。 |
| [set_InsertHeadings](./set_insertheadings/)(bool) | 设置是否将来自数据库的字段名称插入为结果表中的列标题。 |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | 设置是否在合并开始时插入数据。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | 设置要插入的最后一条数据记录的整数记录号。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Query](./set_query/)(const System::String\&) | 设置查询数据库的 SQL 指令集合。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | 设置要应用于数据库查询结果的格式。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
