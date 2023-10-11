---
title: Document.AttachedTemplate
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على أو تعيين المسار الكامل للقالب المرفق بالمستند.
type: docs
weight: 20
url: /ar/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

الحصول على أو تعيين المسار الكامل للقالب المرفق بالمستند.

```csharp
public string AttachedTemplate { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentNullException | يلقي إذا حاولت التعيين على أ`باطل` قيمة. |

### ملاحظات

تعني السلسلة الفارغة أن المستند مرفق بالقالب العادي.

### أمثلة

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


