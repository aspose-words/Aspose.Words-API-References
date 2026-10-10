---
title: "طريقة Aspose::Words::Fields::Field::get_LocaleId"
linktitle: "get_LocaleId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::get_LocaleId. يحصل على أو يضبط معرف اللغة (LCID) للحقل في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


يحصل أو يعيّن معرف اللغة (LCID) للحقل.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## أمثلة



يعرض كيفية إدراج حقل والعمل مع إعداداته الإقليمية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقل DATE، ثم اطبع التاريخ الذي سيعرضه.
// تحدد الثقافة الحالية للخيط الخاص بك تنسيق التاريخ.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// تغيير ثقافة الخيط الخاص بنا سيؤثر على نتيجة حقل DATE.
// طريقة أخرى لجعل حقل DATE يعرض تاريخًا بثقافة مختلفة هي استخدام خاصية LocaleId الخاصة به.
// تتيح لنا هذه الطريقة تجنب تغيير ثقافة الخيط للحصول على هذا التأثير.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
