---
title: "Aspose::Words::Fields::FieldAdvance 类"
linktitle: "FieldAdvance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAdvance 类。实现 ADVANCE 字段。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fields/fieldadvance/
---
## FieldAdvance class


实现 ADVANCE 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldAdvance : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_DownOffset](./get_downoffset/)() | 获取或设置字段后面的文本应向下移动的点数。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_HorizontalPosition](./get_horizontalposition/)() | 获取或设置字段后面的文本应相对于列、框架或文本框左边缘水平移动的点数。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LeftOffset](./get_leftoffset/)() | 获取或设置字段后面的文本应向左移动的点数。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_RightOffset](./get_rightoffset/)() | 获取或设置字段后面的文本应向右移动的点数。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_UpOffset](./get_upoffset/)() | 获取或设置字段后面的文本应向上移动的点数。 |
| [get_VerticalPosition](./get_verticalposition/)() | 获取或设置字段后面的文本应相对于页面顶部垂直移动的点数。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_DownOffset](./set_downoffset/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_DownOffset](./get_downoffset/) 的 setter。 |
| [set_HorizontalPosition](./set_horizontalposition/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition](./get_horizontalposition/) 的 setter。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LeftOffset](./set_leftoffset/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_LeftOffset](./get_leftoffset/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_RightOffset](./set_rightoffset/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_RightOffset](./get_rightoffset/) 的 setter。 |
| [set_UpOffset](./set_upoffset/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_UpOffset](./get_upoffset/) 的 setter。 |
| [set_VerticalPosition](./set_verticalposition/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldAdvance::get_VerticalPosition](./get_verticalposition/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何插入 ADVANCE 字段并编辑其属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// 以下是使用 ADVANCE 字段调整其后文本位置的两种方法。
// ADVANCE 字段的效果会持续应用，直到段落结束，
// 或另一个 ADVANCE 字段更新偏移/坐标值。
// 1 -  指定方向偏移：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  将文本移动到坐标指定的位置：
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
