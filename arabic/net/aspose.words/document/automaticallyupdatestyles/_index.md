---
title: Document.AutomaticallyUpdateStyles
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على أو تعيين علامة تشير إلى ما إذا كانت الأنماط الموجودة في المستند قد تم تحديثها لتتوافق مع الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في برنامج MS Word.
type: docs
weight: 30
url: /ar/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

الحصول على أو تعيين علامة تشير إلى ما إذا كانت الأنماط الموجودة في المستند قد تم تحديثها لتتوافق مع الأنماط الموجودة في القالب المرفق في كل مرة يتم فيها فتح المستند في برنامج MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### أمثلة

يوضح كيفية إرفاق قالب بمستند.

```csharp
Document doc = new Document();

// تأتي مستندات Microsoft Word بشكل افتراضي مع قالب مرفق يسمى "Normal.dotm".
// لا يوجد قالب افتراضي لمستندات Aspose.Words الفارغة.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// قم بإرفاق قالب، ثم قم بتعيين العلامة لتطبيق تغييرات النمط
// داخل القالب للأنماط الموجودة في وثيقتنا.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


