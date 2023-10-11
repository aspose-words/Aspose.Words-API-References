---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words لمراجع .NET API
description: RtfSaveOptions ملكية. يسمح بتصغير حجم مستندات RTF الناتجة ولكن إذا كانت تحتوي على نص RTL من اليمين إلى اليسار فلن يتم عرضه بشكل صحيح. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

يسمح بتصغير حجم مستندات RTF الناتجة، ولكن إذا كانت تحتوي على نص RTL (من اليمين إلى اليسار)، فلن يتم عرضه بشكل صحيح. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ExportCompactSize { get; set; }
```

### ملاحظات

إذا كانت الوثيقة التي تريد تحويلها إلى RTF باستخدام Aspose.Words لا تحتوي على نص من اليمين إلى اليسار بلغات مثل العربية، فيمكنك ضبط هذا الخيار على`حقيقي` لتقليل حجم RTF الناتج.

### أمثلة

يوضح كيفية حفظ مستند إلى .rtf مع خيارات مخصصة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "RtfSaveOptions" لتمريره إلى طريقة "حفظ" المستند لتعديل كيفية حفظه في RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// قم بتعيين خاصية "ExportCompactSize" على "صحيح" to
// تقليل حجم المستند المحفوظ على حساب توافق النص من اليمين إلى اليسار.
options.ExportCompactSize = true;

// قم بتعيين خاصية "ExportImagesFotOldReaders" على "true" لاستخدام كلمات رئيسية إضافية للتأكد من أن وثيقتنا صحيحة
// متوافق مع قارئات ما قبل Microsoft Word 97 وWordPad.
// اضبط الخاصية "ExportImagesFotOldReaders" على "خطأ" لتقليل حجم المستند،
// ولكن يمنع القراء القدامى من قراءة أي صور غير ملف تعريف أو BMP قد يحتوي عليها المستند.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### أنظر أيضا

* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../rtfsaveoptions/)
* المجسم [Aspose.Words](../../../)


