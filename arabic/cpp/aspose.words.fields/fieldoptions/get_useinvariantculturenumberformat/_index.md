---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat طريقة"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat طريقة. يحصل أو يعيّن القيمة التي تشير إلى ما إذا كان تنسيق الأرقام يُفسّر باستخدام ثقافة ثابتة أم لا في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


الحصول على أو تعيين القيمة التي تشير إلى ما إذا كان تنسيق الأرقام يُحلل باستخدام ثقافة ثابتة أم لا.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## ملاحظات


عند تعيين هذه الخاصية إلى **true**، يُؤخذ تنسيق الأرقام من ثقافة ثابتة.

عند تعيين هذه الخاصية إلى **false**، يُؤخذ تنسيق الأرقام من ثقافة الخيط الحالي.

القيمة الافتراضية هي **false**.

## أمثلة



يظهر كيفية تنسيق الأرقام وفقًا للثقافة الثابتة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// أحيانًا، قد لا تقوم الحقول بتنسيق أرقامها بشكل صحيح تحت بعض الثقافات.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// لإصلاح ذلك، يمكننا تغيير الثقافة لكامل الخيط.
// طريقة أخرى لإصلاح ذلك هي تعيين هذا العلم،
// مما يجعل جميع الحقول تستخدم الثقافة الثابتة عند تنسيق الأرقام.
// بهذه الطريقة نتمكن من تجنّب تغيير الثقافة لكامل الخيط.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
