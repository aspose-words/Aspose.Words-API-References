---
title: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders"
linktitle: "get_ExportImagesForOldReaders"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders. تحدد ما إذا كانت الكلمات المفتاحية لـ \"old readers\" تُكتب إلى RTF أم لا. يمكن أن يؤثر ذلك بشكل كبير على حجم مستند RTF. القيمة الافتراضية هي true في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


يحدد ما إذا كانت الكلمات المفتاحية لـ "القراء القدامى" تُكتب إلى RTF أم لا. يمكن أن يؤثر ذلك بشكل كبير على حجم مستند RTF. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## ملاحظات


"Old readers" هي تطبيقات ما قبل Microsoft Word 97 وأيضًا WordPad. عندما يكون هذا الخيار **true** تقوم Aspose.Words بكتابة كلمات مفتاحية إضافية في RTF. تسمح هذه الكلمات المفتاحية بعرض المستند بشكل صحيح عند فتحه في تطبيق "old reader"، ولكن يمكن أن تزيد حجم المستند بشكل كبير.

إذا قمت بتعيين هذا الخيار إلى **false**، فستُعرض فقط الصور بصيغ WMF و EMF و BMP في "old readers".

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
