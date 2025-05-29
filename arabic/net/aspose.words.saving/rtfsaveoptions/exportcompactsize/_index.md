---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words لـ .NET
description: حسّن حجم مستندات RTF باستخدام خاصية ExportCompactSize. وفّر تخزينًا فعالًا مع الحفاظ على سلامة النص، حتى مع محتوى RTL.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

يسمح بجعل مستندات RTF الناتجة أصغر حجمًا، ولكن إذا كانت تحتوي على نص من اليمين إلى اليسار (x000d_ RTL)، فلن يتم عرضها بشكل صحيح. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportCompactSize { get; set; }
```

## ملاحظات

إذا كانت الوثيقة التي تريد تحويلها إلى RTF باستخدام Aspose.Words لا تحتوي على نص من اليمين إلى اليسار في لغات مثل العربية، فيمكنك تعيين هذا الخيار على`حقيقي` لتقليل حجم RTF الناتج.

## أمثلة

يوضح كيفية حفظ مستند بتنسيق .rtf باستخدام خيارات مخصصة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "RtfSaveOptions" لتمريره إلى طريقة "حفظ" المستند لتعديل كيفية حفظه في RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// اضبط خاصية "ExportCompactSize" على "true" لـ
// تقليل حجم المستند المحفوظ على حساب توافق النص من اليمين إلى اليسار.
options.ExportCompactSize = true;

// اضبط خاصية "ExportImagesFotOldReaders" على "true" لاستخدام كلمات رئيسية إضافية لضمان أن مستندنا
// متوافق مع برامج قراءة ما قبل Microsoft Word 97 وWordPad.
// اضبط خاصية "ExportImagesFotOldReaders" على "false" لتقليل حجم المستند،
// ولكن منع القراء القدامى من القدرة على قراءة أي صور غير ملف تعريفي أو صور BMP قد يحتوي عليها المستند.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### أنظر أيضا

* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
