---
title: "Aspose::Words::Fields::FieldFormat 类"
linktitle: "FieldFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldFormat 类。提供对字段的数值、日期和时间以及通用格式的类型化访问。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words.fields/fieldformat/
---
## FieldFormat class


提供对字段的数值、日期和时间以及常规格式的类型化访问。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DateTimeFormat](./get_datetimeformat/)() | 获取或设置应用于日期和时间字段结果的格式。对应 \@ 开关。 |
| [get_GeneralFormats](./get_generalformats/)() | 获取应用于数值、文本或任何字段结果的一组通用格式。对应 \* 开关。 |
| [get_NumericFormat](./get_numericformat/)() | 获取或设置应用于数值字段结果的格式。对应 \# 开关。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DateTimeFormat](./set_datetimeformat/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldFormat::get_DateTimeFormat](./get_datetimeformat/)。 |
| [set_NumericFormat](./set_numericformat/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldFormat::get_NumericFormat](./get_numericformat/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何格式化字段结果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入一个字段，以显示未应用任何格式的结果。
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// 我们可以使用字段的属性为字段结果应用格式。
// 下面是我们可以应用于字段结果的三种格式类型。
// 1 - 数值格式：
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 - 日期/时间格式：
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 - 常规格式：
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// 我们可以移除格式，将字段结果恢复到原始形式。
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
