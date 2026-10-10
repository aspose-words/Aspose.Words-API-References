---
title: "Aspose::Words::Document::get_AttachedTemplate طريقة"
linktitle: "get_AttachedTemplate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::get_AttachedTemplate طريقة. يحصل أو يحدد المسار الكامل للقالب المرفق بالمستند في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


يحصل أو يعيّن المسار الكامل للقالب المرفق بالمستند.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## ملاحظات


السلسلة الفارغة تعني أن المستند مرفق بالقالب Normal.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
