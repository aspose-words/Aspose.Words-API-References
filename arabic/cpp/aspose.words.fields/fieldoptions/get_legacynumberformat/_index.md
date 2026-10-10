---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat طريقة"
linktitle: "get_LegacyNumberFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat method. يحصل على أو يضبط القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول مفعلاً أم لا في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول مفعلاً أم لا.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## ملاحظات


عندما يتم ضبط هذه الخاصية على **true**، يعمل رمز القالب \"#\" كما في .net: يستبدل علامة الجنيه بالرقم المقابل إذا كان موجودًا؛ وإلا، لا تظهر أي رموز في سلسلة النتيجة.

عندما يتم ضبط هذه الخاصية على **false**، يعمل رمز القالب \"#\" كما في MS Word: يحدد عنصر التنسيق الأماكن الرقمية المطلوبة للعرض في النتيجة. إذا لم تتضمن النتيجة رقمًا في ذلك الموضع، يعرض MS Word مسافة. على سبيل المثال، { = 9 + 6 \\# $### } يعرض $ 15.

القيمة الافتراضية هي **false**.

## أمثلة



يوضح كيفية تمكين تنسيق الأرقام القديم للحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
