---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خاصية Document AttachedTemplate بكفاءة. حدّد أو استرجاع المسار الكامل لقالب مستندك بسهولة لضمان تكامل سلس.
type: docs
weight: 20
url: /ar/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

يحصل على المسار الكامل للقالب المرفق بالمستند أو يعينه.

```csharp
public string AttachedTemplate { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يتم طرحه إذا حاولت التعيين على`باطل` قيمة. |

## ملاحظات

تعني السلسلة الفارغة أن المستند مرفق بالقالب العادي.

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

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
