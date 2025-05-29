---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.RunCollection للوصول بسلاسة إلى عُقد التشغيل. حسّن معالجة مستنداتك بميزات قوية ومكتوبة!
type: docs
weight: 5570
url: /ar/net/aspose.words/runcollection/
---
## RunCollection class

يوفر وصولاً مكتوبًا إلى مجموعة من[`Run`](../run/) العقد.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class RunCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/runcollection/item/) { get; } | يسترجع[`Run`](../run/) عند الفهرس المعطى. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | يعيد الفهرس المبني على الصفر للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | نسخ جميع عمليات التشغيل من المجموعة إلى مجموعة جديدة من عمليات التشغيل. (2 methods) |

## أمثلة

يوضح كيفية تحديد نوع المراجعة لعقدة مضمنة.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// عندما نقوم بتحرير المستند أثناء وجود خيار "تعقب التغييرات"، الموجود عبر المراجعة -> التعقب،
// إذا تم تشغيله في Microsoft Word، فإن التغييرات التي نطبقها تعتبر بمثابة مراجعات.
// عند تحرير مستند باستخدام Aspose.Words، يمكننا البدء في تتبع المراجعات من خلال
// استدعاء طريقة "StartTrackRevisions" الخاصة بالمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
// يمكننا إما قبول المراجعات لاستيعابها في المستند
// أو رفضهم لتغيير التغيير المقترح بشكل فعال.
Assert.AreEqual(6, doc.Revisions.Count);

// العقدة الأصلية للمراجعة هي التشغيل الذي يتعلق به. التشغيل هو عقدة مضمنة.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// فيما يلي خمسة أنواع من المراجعات التي يمكنها الإشارة إلى عقدة مضمنة.
// 1 - مراجعة "إدراج":
// يحدث هذا التعديل عندما نقوم بإدراج نص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - مراجعة "التنسيق":
// يحدث هذا التعديل عندما نقوم بتغيير تنسيق النص أثناء تتبع التغييرات.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - مراجعة "الانتقال من":
// عندما نقوم بتمييز النص في Microsoft Word، ثم نقوم بسحبه إلى مكان مختلف في المستند
// أثناء تتبع التغييرات، يظهر نسختان.
// إن النسخة المعدلة "نقل من" هي نسخة من النص الأصلي قبل نقله.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - مراجعة "الانتقال إلى":
// إن المراجعة "نقل إلى" هي النص الذي نقلناه إلى موضعه الجديد في المستند.
// تظهر مراجعات "الانتقال من" و"الانتقال إلى" في أزواج لكل مراجعة نقل نقوم بتنفيذها.
// يؤدي قبول مراجعة النقل إلى حذف مراجعة "النقل من" ونصها،
// ويحتفظ بالنص من المراجعة "نقل إلى".
// على العكس من ذلك، يؤدي رفض مراجعة النقل إلى الاحتفاظ بمراجعة "النقل من" وحذف مراجعة "النقل إلى".
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - مراجعة "حذف":
// يحدث هذا التعديل عند حذف نص أثناء تتبع التغييرات. عند حذف نص بهذه الطريقة،
// سوف تبقى في المستند كمراجعة حتى نقبل المراجعة،
// والذي سوف يقوم بحذف النص نهائيا، أو رفض المراجعة، مما سوف يبقي النص الذي قمنا بحذفه حيث كان.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
