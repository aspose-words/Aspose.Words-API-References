---
title: "فئة Aspose::Words::Fields::FieldFormat"
linktitle: "FieldFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldFormat. توفر وصولًا مكتوبًا إلى القيم الرقمية، التاريخ والوقت، والتنسيق العام للحقل. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words.fields/fieldformat/
---
## FieldFormat class


يوفر وصولًا مكتوبًا إلى تنسيقات الحقل الرقمية وتاريخ ووقت وتنسيق عام. لمعرفة المزيد، قم بزيارة [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldFormat : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DateTimeFormat](./get_datetimeformat/)() | يحصل أو يعيّن تنسيقًا يُطبق على نتيجة حقل التاريخ والوقت. يتوافق مع المفتاح \@. |
| [get_GeneralFormats](./get_generalformats/)() | يحصل على مجموعة من التنسيقات العامة التي تُطبق على نتيجة حقل رقمي أو نصي أو أي حقل. يتوافق مع المفاتيح \*. |
| [get_NumericFormat](./get_numericformat/)() | يحصل أو يعيّن تنسيقًا يُطبق على نتيجة حقل رقمي. يتوافق مع المفتاح \#. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DateTimeFormat](./set_datetimeformat/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldFormat::get_DateTimeFormat](./get_datetimeformat/). |
| [set_NumericFormat](./set_numericformat/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldFormat::get_NumericFormat](./get_numericformat/). |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية تنسيق نتائج الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم منشئ المستند لإدراج حقل يعرض نتيجة بدون تطبيق أي تنسيق.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// يمكننا تطبيق تنسيق على نتيجة الحقل باستخدام خصائص الحقل.
// فيما يلي ثلاثة أنواع من التنسيقات التي يمكننا تطبيقها على نتيجة الحقل.
// 1 -  تنسيق رقمي:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  تنسيق تاريخ/وقت:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  تنسيق عام:
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

// يمكننا إزالة تنسيقاتنا لإعادة نتيجة الحقل إلى شكلها الأصلي.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
