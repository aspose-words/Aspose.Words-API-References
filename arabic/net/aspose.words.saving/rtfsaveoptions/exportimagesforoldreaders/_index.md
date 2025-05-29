---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words لـ .NET
description: حسّن مستندات RTF باستخدام خاصية ExportImagesForOldReaders. تحكّم في تضمين الكلمات المفتاحية للقارئات القديمة، مما يؤثر على حجم الملف وأدائه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

يحدد ما إذا كانت الكلمات الأساسية لـ "القراء القدامى" مكتوبة في RTF أم لا. يمكن أن يؤثر هذا بشكل كبير على حجم مستند RTF. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## ملاحظات

"القراء القدامى" هي تطبيقات ما قبل Microsoft Word 97 وWordPad أيضًا. عندما يكون هذا الخيار متاحًا`حقيقي` يكتب Aspose.Words كلمات رئيسية إضافية لـ RTF. تسمح هذه الكلمات الرئيسية بعرض المستند بشكل صحيح عند فتحه في تطبيق "القارئ القديم" ، ولكنها قد تزيد بشكل كبير من حجم المستند.

إذا قمت بتعيين هذا الخيار على`خطأ شنيع`، ثم سيتم عرض الصور بتنسيقات WMF وEMF وBMP فقط في "القراء القدامى".

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
