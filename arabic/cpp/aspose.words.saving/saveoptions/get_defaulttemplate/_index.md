---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate method"
linktitle: "get_DefaultTemplate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate method. يحصل على أو يضبط مسار القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي سلسلة فارغة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


يحصل أو يعيّن المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


## أمثلة



يظهر كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// فعّل تحديث الأنماط تلقائيًا، لكن لا تُرفق مستند قالب.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// نظرًا لعدم وجود مستند قالب، لم يكن للمستند مكان لتتبع تغييرات النمط.
// استخدم كائن SaveOptions لتعيين قالب تلقائيًا
// إذا كان المستند الذي نقوم بحفظه لا يحتوي على واحد.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
