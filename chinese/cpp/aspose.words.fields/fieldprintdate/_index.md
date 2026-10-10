---
title: "Aspose::Words::Fields::FieldPrintDate 类"
linktitle: "FieldPrintDate"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldPrintDate 类。实现 PRINTDATE 字段。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 81000
url: /zh/cpp/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class


实现 PRINTDATE 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldPrintDate : public Aspose::Words::Fields::Field,
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
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | 用于设置 [Aspose::Words::Fields::FieldPrintDate::get_UseLunarCalendar](./get_uselunarcalendar/)。 |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | 用于设置 [Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/)。 |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | 用于设置 [Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



显示已读取的 PRINTDATE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// 当文档通过打印机打印或打印为 PDF（但未导出为 PDF）时，
// PRINTDATE 字段将显示打印操作的日期/时间。
// 如果未进行打印，这些字段将显示 "0/0/0000"。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// 以下是根据 PRINTDATE 字段的三种不同日历类型
// 可以显示上一次打印操作的日期和时间。
// 1 - 伊斯兰阴历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura 日历：
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  印度国家日历：
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
