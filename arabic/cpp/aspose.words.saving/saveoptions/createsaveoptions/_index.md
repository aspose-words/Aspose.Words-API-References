---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions طريقة"
linktitle: "CreateSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions method. ينشئ كائن خيارات حفظ من فئة مناسبة لتنسيق الحفظ المحدد في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


ينشئ كائن خيارات حفظ من فئة مناسبة للصيغة المحددة للحفظ.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | تنسيق الحفظ الذي سيتم إنشاء كائن خيارات حفظ له. |

### ReturnValue

كائن من فئة مشتقة من [SaveOptions](../).

## انظر أيضًا

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


ينشئ كائن خيارات حفظ من فئة مناسبة لامتداد الملف المحدد في اسم الملف المعطى.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | امتداد اسم الملف هذا يحدد فئة كائن خيارات الحفظ الذي سيتم إنشاؤه. |

### ReturnValue

كائن من فئة مشتقة من [SaveOptions](../).

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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
