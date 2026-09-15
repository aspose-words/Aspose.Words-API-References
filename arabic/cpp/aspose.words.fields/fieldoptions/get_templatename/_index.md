---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName طريقة"
linktitle: "get_TemplateName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName method. يحصل أو يضبط اسم ملف القالب المستخدم من قبل المستند في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


الحصول على أو تعيين اسم ملف القالب المستخدم في المستند.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## ملاحظات


هذه الخاصية تُستخدم بواسطة حقل [FieldTemplate](../../fieldtemplate/) إذا كانت خاصية [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) فارغة.

إذا كانت هذه الخاصية فارغة، يُستخدم اسم ملف القالب الافتراضي **Normal.dotm**.

## أمثلة



يظهر كيفية استخدام حقل TEMPLATE لعرض موقع نظام الملفات المحلي لقالب المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكننا تعيين اسم القالب باستخدام الحقول. تُستخدم هذه الخاصية عندما تكون "doc.AttachedTemplate" فارغة.
// إذا كانت هذه الخاصية فارغة، يُستخدم اسم ملف القالب الافتراضي "Normal.dotm".
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
