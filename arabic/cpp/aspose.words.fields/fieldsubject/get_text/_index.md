---
title: "طريقة Aspose::Words::Fields::FieldSubject::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldSubject::get_Text. يحصل أو يضبط نص الموضوع في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


يحصل أو يعيّن نص الموضوع.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## أمثلة



يوضح كيفية استخدام حقل SUBJECT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عيّن قيمة لخاصية \"Subject\" المدمجة في المستند.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// أنشئ حقل SUBJECT لعرض قيمة تلك الخاصية المدمجة.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// إذا قمنا بإعطاء خاصية Text لحقل SUBJECT قيمة وقمنا بتحديثها، فإن الحقل سي
// يستبدل القيمة الحالية للخاصية المدمجة "Subject" بقيمة خاصية Text الخاصة به،
// ثم تعرض القيمة الجديدة.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## انظر أيضًا

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
