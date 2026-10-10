---
title: "Aspose::Words::Fields::FieldDate 类"
linktitle: "FieldDate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldDate 类。实现 DATE 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words.fields/fielddate/
---
## FieldDate class


实现 DATE 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldDate : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                  public Aspose::Words::Fields::IFieldWithCalendar
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_UseLastFormat](./get_uselastformat/)() | 获取或设置在插入新 DATE 字段时是否使用宿主应用程序上次使用的格式。 |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() override | 获取或设置是否使用伊斯兰阴历或希伯来阴历。 |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() override | 获取或设置是否使用 Saka 纪元历。 |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() override | 获取或设置是否使用 Um-al-Qura 日历。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_UseLastFormat](./set_uselastformat/)(bool) | 设置 [Aspose::Words::Fields::FieldDate::get_UseLastFormat](./get_uselastformat/)。 |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | 设置 [Aspose::Words::Fields::FieldDate::get_UseLunarCalendar](./get_uselunarcalendar/)。 |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | 设置 [Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/)。 |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | 设置 [Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 DATE 字段根据不同类型的日历显示日期。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们希望文档中的文本始终显示正确的日期，可以使用 DATE 字段。
// 以下是 DATE 字段可以用来显示日期的三种文化日历类型。
// 1 - 伊斯兰阴历：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura 日历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  印度国家日历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// 插入一个 DATE 字段并将其日历类型设置为主机应用程序上次使用的类型。
// 在 Microsoft Word 中，该类型将是最近在 Insert -> Text -> Date and Time 对话框中使用的类型。
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
