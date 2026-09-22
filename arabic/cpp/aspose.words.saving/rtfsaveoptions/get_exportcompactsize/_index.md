---
title: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize"
linktitle: "get_ExportCompactSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize. تسمح بجعل مستندات RTF الناتجة أصغر حجمًا، ولكن إذا احتوت على نص RTL (من اليمين إلى اليسار) فلن يتم عرضها بشكل صحيح. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


يسمح بجعل مستندات RTF الناتجة أصغر حجماً، ولكن إذا احتوت على نص RTL (من اليمين إلى اليسار) فلن يتم عرضها بشكل صحيح. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## ملاحظات


إذا كان المستند الذي تريد تحويله إلى RTF باستخدام Aspose.Words لا يحتوي على نص من اليمين إلى اليسار في لغات مثل العربية، يمكنك ضبط هذا الخيار إلى **true** لتقليل حجم ملف RTF الناتج.

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

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
