---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تضمن خاصية AutomaticallyUpdateStyles في MS Word مزامنة أنماط مستندك مع القالب في كل مرة تفتحه، مما يعزز الاتساق.
type: docs
weight: 30
url: /ar/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

يحصل على علم أو يعينه للإشارة إلى ما إذا كانت الأنماط في المستند يتم تحديثها لتتوافق مع الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## أمثلة

يوضح كيفية إرفاق قالب بالمستند.

```csharp
Document doc = new Document();

// تأتي مستندات Microsoft Word بشكل افتراضي مع قالب مرفق يسمى "Normal.dotm".
// لا يوجد قالب افتراضي لمستندات Aspose.Words الفارغة.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// قم بإرفاق قالب، ثم قم بتعيين العلم لتطبيق تغييرات النمط
// ضمن القالب إلى الأنماط الموجودة في مستندنا.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
