---
title: "طريقة Aspose::Words::Fields::FieldInfo::get_NewValue"
linktitle: "get_NewValue"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldInfo::get_NewValue. يحصل أو يعيّن قيمة اختيارية تُحدّث الخاصية في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldinfo/get_newvalue/
---
## FieldInfo::get_NewValue method


يحصل أو يضبط قيمة اختيارية تقوم بتحديث الخاصية.

```cpp
System::String Aspose::Words::Fields::FieldInfo::get_NewValue()
```


## أمثلة



يوضح كيفية العمل مع حقول INFO.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عيّن قيمة للخاصية المدمجة "Comments" ثم أدخل حقل INFO لعرض قيمة تلك الخاصية.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->Update();

ASSERT_EQ(u" INFO  Comments", field->GetFieldCode());
ASSERT_EQ(u"My comment", field->get_Result());

builder->Writeln();

// تعيين قيمة لخاصية NewValue الخاصة بالحقل وتحديث
// سيقوم الحقل أيضًا بالكتابة فوق الخاصية المدمجة المقابلة بالقيمة الجديدة.
field = System::ExplicitCast<Aspose::Words::Fields::FieldInfo>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInfo, true));
field->set_InfoType(u"Comments");
field->set_NewValue(u"New comment");
field->Update();

ASSERT_EQ(u" INFO  Comments \"New comment\"", field->GetFieldCode());
ASSERT_EQ(u"New comment", field->get_Result());
ASSERT_EQ(u"New comment", doc->get_BuiltInDocumentProperties()->get_Comments());

doc->Save(get_ArtifactsDir() + u"Field.INFO.docx");
```

## انظر أيضًا

* Class [FieldInfo](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
