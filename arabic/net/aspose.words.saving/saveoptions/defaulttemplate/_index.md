---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words لـ .NET
description: أدر خيارات الحفظ بسهولة! عيّن أو احصل على مسار القالب واسم الملف الافتراضيين لمعالجة مستنداتك بسلاسة. حسّن سير عملك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

يحصل على المسار إلى القالب الافتراضي (بما في ذلك اسم الملف) أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## ملاحظات

إذا تم تحديد ذلك، فسيتم استخدام هذا المسار لتحميل القالب عند[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) يكون`حقيقي` ، لكن[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) فارغ.

## أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين تحديث النمط التلقائي، ولكن لا تقم بإرفاق مستند قالب.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب، لم يكن لدى المستند مكان لتتبع تغييرات الأسلوب.
// استخدم كائن SaveOptions لتعيين قالب تلقائيًا
// إذا كان المستند الذي نحفظه لا يحتوي على واحد.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
