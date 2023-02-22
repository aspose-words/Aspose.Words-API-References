---
title: RtfSaveOptions.SaveFormat
second_title: Aspose.Words لمراجع .NET API
description: RtfSaveOptions ملكية. يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونRtf .
type: docs
weight: 40
url: /ar/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ . يمكن فقط أن يكونRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../rtfsaveoptions/)
* المجسم [Aspose.Words](../../../)


