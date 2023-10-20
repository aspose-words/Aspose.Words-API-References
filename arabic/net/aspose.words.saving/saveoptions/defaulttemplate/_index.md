---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words لـ .NET
description: SaveOptions DefaultTemplate ملكية. الحصول على أو تعيين المسار إلى القالب الافتراضي بما في ذلك اسم الملف. القيمة الافتراضية لهذه الخاصية هيسلسلة فارغة Empty في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

الحصول على أو تعيين المسار إلى القالب الافتراضي (بما في ذلك اسم الملف). القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

## ملاحظات

إذا تم تحديده، فسيتم استخدام هذا المسار لتحميل القالب عندما[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) يكون`حقيقي` , لكن[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) فارغ.

## أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين التحديث التلقائي للنمط، ولكن لا ترفق مستند القالب.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب، لم يكن للمستند مكان لتتبع تغييرات النمط.
// استخدم كائن SaveOptions لتعيين القالب تلقائيًا
// إذا كانت الوثيقة التي نقوم بحفظها لا تحتوي على واحدة.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
