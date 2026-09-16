---
title: "Aspose::Words::Fields::Field 类"
linktitle: "字段"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field 类。表示 Microsoft Word 文档字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fields/field/
---
## Field class


表示 Microsoft Word 文档字段。要了解更多，请访问文档文章。

```cpp
class Field : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](./get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](./get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](./get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](./get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](./get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](./get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](./get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](./get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](./get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](./get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](./get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](./getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](./getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_IsDirty](./set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/) 的 setter。 |
| [set_IsLocked](./set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/) 的 setter。 |
| [set_LocaleId](./set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/) 的 setter。 |
| [set_Result](./set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](./get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | 执行字段的取消链接。 |
| [Update](./update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](./update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 备注


Word 文档中的字段是一种复杂结构，由多个节点组成，包括字段开始、字段代码、字段分隔符、字段结果和字段结束。[Fields](../) 可以嵌套，包含丰富内容，并跨越文档中的多个段落或节。[Field](./) 类是一个“外观”对象，提供属性和方法，使能够将字段视为单个对象进行操作。

这些 [Start](./get_start/)、[Separator](./get_separator/) 和 [End](./get_end/) 属性分别指向字段的开始、分隔符和结束节点。

字段开始和分隔符之间的内容是字段代码。字段分隔符和字段结束之间的内容是字段结果。字段代码通常由一个或多个 [Run](../../aspose.words/run/) 对象组成，这些对象指定指令。处理应用程序应执行字段代码以计算字段结果。

计算字段结果的过程称为字段更新。Aspose.Words 可以以与 Microsoft Word 完全相同的方式更新大多数字段类型的字段结果。尤其是，Aspose.Words 能够计算即使是最复杂的公式字段的结果。要计算单个字段的字段结果，请使用 [Update](./update/) 方法。要更新整个文档中的字段，请使用 [UpdateFields](../../aspose.words/document/updatefields/) 。

您可以使用 [GetFieldCode()](./getfieldcode/) 方法获取字段代码的纯文本版本。您可以使用 [Result](./get_result/) 属性获取和设置字段结果的纯文本版本。字段代码和字段结果都可以包含复杂内容，例如嵌套字段、段落、形状、表格，在这种情况下，如果需要更多控制，您可能希望直接操作字段节点。

您不能直接创建 [Field](./) 类的实例。要创建新字段，请使用 [InsertField()](../) 方法。

## 示例



展示如何使用字段代码向文档插入字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// 此 InsertField 方法的重载会自动更新插入的字段。
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
