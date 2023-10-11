---
title: RtfSaveOptions.ExportImagesForOldReaders
second_title: Aspose.Words لمراجع .NET API
description: RtfSaveOptions ملكية. يحدد ما إذا كانت الكلمات الأساسية لـ القراء القدامى مكتوبة في RTF أم لا. يمكن أن يؤثر هذا بشكل كبير على حجم مستند RTF. القيمة الافتراضية هيحقيقي .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

يحدد ما إذا كانت الكلمات الأساسية لـ "القراء القدامى" مكتوبة في RTF أم لا. يمكن أن يؤثر هذا بشكل كبير على حجم مستند RTF. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

### ملاحظات

"القراء القدامى" هم تطبيقات ما قبل Microsoft Word 97 وأيضًا WordPad. عندما يكون هذا الخيار`حقيقي` يقوم Aspose.Words بكتابة كلمات RTF إضافية. تسمح هذه الكلمات الأساسية بعرض المستند بشكل صحيح عند فتحه في تطبيق "القارئ القديم"، ولكنها يمكن أن تزيد حجم المستند بشكل ملحوظ.

إذا قمت بتعيين هذا الخيار ل`خطأ شنيع`، فسيتم عرض الصور بتنسيقات WMF وEMF وBMP فقط في "أجهزة القراءة القديمة".

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


