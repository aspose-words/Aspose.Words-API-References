---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath طريقة"
linktitle: "get_IncludeFullPath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath طريقة. يحصل أو يحدد ما إذا كان يجب تضمين اسم مسار الملف الكامل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


يحصل أو يضبط ما إذا كان يجب تضمين اسم مسار الملف الكامل.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
