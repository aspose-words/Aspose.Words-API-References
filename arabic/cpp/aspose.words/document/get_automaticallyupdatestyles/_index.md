---
title: "طريقة Aspose::Words::Document::get_AutomaticallyUpdateStyles"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_AutomaticallyUpdateStyles. يحصل على أو يضبط علامة تشير إلى ما إذا كانت الأنماط في المستند يتم تحديثها لتطابق الأنماط في القالب المرفق في كل مرة يتم فيها فتح المستند في MS Word في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


يحصل أو يعيّن علامة تشير إلى ما إذا كانت الأنماط في المستند تُحدّث لتطابق الأنماط في القالب المرفق في كل مرة يُفتح فيها المستند في MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## أمثلة



يوضح كيفية إرفاق قالب بمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تأتي مستندات Microsoft Word بشكل افتراضي مع قالب مرفق يُدعى "Normal.dotm".
// لا يوجد قالب افتراضي للمستندات الفارغة في Aspose.Words.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// أرفق قالبًا، ثم اضبط العلامة لتطبيق تغييرات الأنماط
// داخل القالب إلى الأنماط في مستندنا.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
