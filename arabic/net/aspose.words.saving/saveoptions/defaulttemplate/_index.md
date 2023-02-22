---
title: SaveOptions.DefaultTemplate
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على أو تعيين المسار للقالب الافتراضي بما في ذلك اسم الملف . القيمة الافتراضية لهذه الخاصية هي سلسلة فارغة Empty  .
type: docs
weight: 40
url: /ar/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

الحصول على أو تعيين المسار للقالب الافتراضي (بما في ذلك اسم الملف) . القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty ) .

```csharp
public string DefaultTemplate { get; set; }
```

### ملاحظات

إذا تم تحديده ، فسيتم استخدام هذا المسار لتحميل القالب عند[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) هذا صحيح ، لكن[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) فارغ.

### أمثلة

يوضح كيفية تعيين قالب افتراضي للمستندات التي لا تحتوي على قوالب مرفقة.

```csharp
Document doc = new Document();

// تمكين التحديث التلقائي للنمط ، لكن لا تقم بإرفاق مستند نموذج.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// نظرًا لعدم وجود مستند قالب ، لم يكن للمستند أي مكان لتعقب تغييرات النمط.
// استخدم كائن SaveOptions لتعيين قالب تلقائيًا
// إذا كان المستند الذي نحفظه لا يحتوي على واحد.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


