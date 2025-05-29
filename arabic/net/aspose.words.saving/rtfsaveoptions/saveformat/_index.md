---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SaveFormat في RtfSaveOptions لحفظ مستنداتك بسهولة بتنسيق RTF، مما يضمن التوافق والمشاركة السهلة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
