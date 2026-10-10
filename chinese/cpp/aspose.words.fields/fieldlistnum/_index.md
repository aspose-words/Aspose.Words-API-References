---
title: "Aspose::Words::Fields::FieldListNum 类"
linktitle: "FieldListNum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldListNum 类。实现 LISTNUM 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 64000
url: /zh/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


实现 LISTNUM 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_HasListName](./get_haslistname/)() | 返回一个值，指示字段代码是否提供了抽象编号定义的名称。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_ListLevel](./get_listlevel/)() | 获取或设置列表中的级别，覆盖字段的默认行为。 |
| [get_ListName](./get_listname/)() | 获取或设置用于编号的抽象编号定义的名称。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_StartingNumber](./get_startingnumber/)() | 获取或设置此字段的起始值。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/) 的 Setter。 |
| [set_ListName](./set_listname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/) 的 Setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/) 的 Setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 LISTNUM 字段为段落编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM 字段显示一个在每个 LISTNUM 字段递增的数字。
// 这些字段还具有多种选项，使我们能够使用它们来模拟编号列表。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// 列表默认从 1 开始计数，但我们可以将此数字设置为其他值，例如 0。
// 此字段将显示 "0)"。
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM 字段为每个列表级别维护独立计数。
// 在与另一个 LISTNUM 字段相同的段落中插入 LISTNUM 字段
// 会增加列表级别而不是计数。
// 下一个字段将继续我们在上面开始的计数，并在列表级别 1 显示值 \"1\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// 此字段将在列表级别 2 开始计数。它将显示值 \"1\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// 此字段将在列表级别 3 开始计数。它将显示值 \"1\"。
// 不同的列表级别有不同的格式，
// 因此这些字段组合后将显示值 \"1)a)i)\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// 我们插入的下一个 LISTNUM 字段将继续该列表级别的计数
// 即前一个 LISTNUM 字段所在的列表级别。
// 我们可以使用 \"ListLevel\" 属性跳转到不同的列表级别。
// 如果此 LISTNUM 字段保持在列表级别 3，它将显示 \"ii)\"，
// 但由于我们已将其移动到列表级别 2，它将在该级别继续计数并显示 \"b)\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// 我们可以设置 ListName 属性，使字段模拟不同的 AUTONUM 字段类型。
// \"NumberDefault\" 模拟 AUTONUM，\"OutlineDefault\" 模拟 AUTONUMOUT，
// 并且 \"LegalDefault\" 模拟 AUTONUMLGL 字段。
// 使用起始数字 1 的 \"OutlineDefault\" 列表名称将显示为 \"I.\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// ListName 不会从前一个字段继承，因此我们需要为每个新字段设置它。
// 此字段使用不同的列表名称继续计数，并显示 \"II.\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
