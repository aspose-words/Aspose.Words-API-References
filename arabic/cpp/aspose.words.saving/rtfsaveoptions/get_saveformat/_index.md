---
title: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat. تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط Rtf في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


تحدد الصيغة التي سيُحفظ بها المستند إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن تكون فقط [Rtf](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


## أمثلة



يظهر كيفية حفظ مستند إلى .rtf باستخدام خيارات مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// أنشئ كائن "RtfSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمستند لتعديل طريقة حفظه كملف RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// اضبط الخاصية "ExportCompactSize" إلى "true" لتـ
// تقليل حجم المستند المحفوظ على حساب توافق النص من اليمين إلى اليسار.
options->set_ExportCompactSize(true);

// اضبط الخاصية "ExportImagesFotOldReaders" إلى "true" لاستخدام كلمات مفتاحية إضافية لضمان أن المستند الخاص بنا هو
// متوافق مع القارئات التي تسبق Microsoft Word 97 وWordPad.
// اضبط الخاصية "ExportImagesFotOldReaders" إلى "false" لتقليل حجم المستند،
// ولكن يمنع القارئات القديمة من القدرة على قراءة أي صور غير ميتافايل أو BMP قد يحتويها المستند.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
