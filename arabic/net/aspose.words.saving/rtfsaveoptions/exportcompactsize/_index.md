---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words لمراجع .NET API
description: RtfSaveOptions ملكية. يسمح بجعل حجم مستندات RTF الإخراج أصغر  ولكن إذا كانت تحتوي على نص RTL من اليمين إلى اليسار  فلن يتم عرضها بشكل صحيح. القيمة الافتراضية هيخاطئة .
type: docs
weight: 20
url: /ar/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

يسمح بجعل حجم مستندات RTF الإخراج أصغر ، ولكن إذا كانت تحتوي على نص RTL (من اليمين إلى اليسار) ، فلن يتم عرضها بشكل صحيح. القيمة الافتراضية هي`خاطئة` .

```csharp
public bool ExportCompactSize { get; set; }
```

### ملاحظات

إذا كان المستند الذي تريد تحويله إلى RTF باستخدام Aspose. لا تحتوي الكلمات على نص من اليمين إلى اليسار بلغات مثل العربية ، فيمكنك ضبط هذا الخيار على`حقيقي` لتقليل حجم RTF الناتج.

### أمثلة

يوضح كيفية حفظ مستند في .rtf بخيارات مخصصة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "RtfSaveOptions" لتمريره إلى أسلوب "Save" الخاص بالمستند لتعديل كيفية حفظه في RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// اضبط خاصية "ExportCompactSize" على "true" إلى
// تقليل حجم المستند المحفوظ على حساب توافق النص من اليمين إلى اليسار.
options.ExportCompactSize = true;

// اضبط خاصية "ExportImagesFotOldReaders" على "true" لاستخدام كلمات رئيسية إضافية للتأكد من أن وثيقتنا
// متوافق مع أجهزة قراءة ما قبل Microsoft Word 97 و WordPad.
// اضبط خاصية "ExportImagesFotOldReaders" على "خطأ" لتقليل حجم المستند ،
// ولكن تمنع القراء القدامى من قراءة أي صور غير ملفات تعريف أو صور BMP قد يحتوي عليها المستند.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### أنظر أيضا

* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../rtfsaveoptions/)
* المجسم [Aspose.Words](../../../)


