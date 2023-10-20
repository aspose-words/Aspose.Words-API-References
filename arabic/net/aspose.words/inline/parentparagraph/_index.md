---
title: Inline.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words لـ .NET
description: Inline ParentParagraph ملكية. يسترد الأصلParagraph من هذه العقدة في C#.
type: docs
weight: 70
url: /ar/net/aspose.words/inline/parentparagraph/
---
## Inline.ParentParagraph property

يسترد الأصل[`Paragraph`](../../paragraph/) من هذه العقدة.

```csharp
public Paragraph ParentParagraph { get; }
```

## أمثلة

يوضح كيفية تحديد نوع المراجعة للعقدة المضمنة.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تتبع التغييرات" عبر المراجعة -> تتبع،
// قيد التشغيل في Microsoft Word، والتغييرات التي نطبقها تعتبر مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات بواسطة
// استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا قبول المراجعات لاستيعابها في المستند
// أو ارفضها لتغيير التغيير المقترح بشكل فعال.
Assert.AreEqual(6, doc.Revisions.Count);

// العقدة الأصلية للمراجعة هي التشغيل الذي تتعلق به المراجعة. التشغيل هو عقدة مضمنة.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها وضع علامة على العقدة المضمنة.
// 1 - مراجعة "إدراج":
// تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - مراجعة "التنسيق":
// تحدث هذه المراجعة عندما نقوم بتغيير تنسيق النص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، تظهر مراجعتان.
// مراجعة "النقل من" هي نسخة من النص في الأصل قبل نقله.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - مراجعة "الانتقال إلى":
// المراجعة "الانتقال إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من مراجعة "الانتقال إلى".
// يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "الانتقال من" وحذف مراجعة "الانتقال إلى".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - مراجعة "الحذف":
// تحدث هذه المراجعة عندما نقوم بحذف النص أثناء تتبع التغييرات. عندما نقوم بحذف نص مثل هذا،
// سيبقى في المستند كمراجعة حتى نقبل المراجعة،
// مما سيؤدي إلى حذف النص نهائيًا، أو رفض المراجعة، مما سيبقي النص الذي حذفناه حيث كان.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [Inline](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
