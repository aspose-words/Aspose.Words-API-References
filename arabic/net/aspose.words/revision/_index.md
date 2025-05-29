---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Revision لإدارة التغييرات المُتتبَّعة في المستندات. حدّد أنواع المراجعات بسهولة لتحرير مستنداتك بسلاسة.
type: docs
weight: 5500
url: /ar/net/aspose.words/revision/
---
## Revision class

يمثل مراجعة (تغيير متعقب) في عقدة مستند أو نمط. استخدم[`RevisionType`](./revisiontype/) للتحقق من نوع هذه المراجعة.

لمعرفة المزيد، قم بزيارة[تعقب التغييرات في المستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public class Revision
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | يحصل على مؤلف هذه المراجعة أو يعيّنه. لا يمكن أن يكون سلسلة فارغة أو`باطل` . |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | يحصل على تاريخ/وقت هذه المراجعة أو يعينه. |
| [Group](../../aspose.words/revision/group/) { get; } | يحصل على مجموعة المراجعة. يُرجع`باطل` إذا لم تكن المراجعة تنتمي إلى أي مجموعة. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | يحصل على العقدة الأصلية المباشرة (المالك) لهذه المراجعة. ستعمل هذه الخاصية مع أي نوع مراجعة آخر غيرStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | يحصل على نمط الوالد المباشر (المالك) لهذه المراجعة. ستعمل هذه الخاصية فقط لـStyleDefinitionChange نوع المراجعة. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | يحصل على نوع هذه المراجعة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | يقبل هذه المراجعة. |
| [Reject](../../aspose.words/revision/reject/)() | رفض هذه المراجعة. |

## أمثلة

يوضح كيفية العمل مع المراجعات في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//التحرير العادي للمستند لا يعتبر مراجعة.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// لتسجيل تعديلاتنا كمراجعات، نحتاج إلى إعلان المؤلف، ثم البدء في تعقبها.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// يتوافق هذا العلم مع خيار "المراجعة" -> "التتبع" -> "تعقب التغييرات" في Microsoft Word.
// لا تؤثر طريقة "StartTrackRevisions" على قيمتها،
// والمستند يتتبع المراجعات برمجيًا على الرغم من وجود قيمة "false".
// إذا فتحنا هذا المستند باستخدام Microsoft Word، فلن يتمكن من تتبع المراجعات.
Assert.IsFalse(doc.TrackRevisions);

// لقد أضفنا نصًا باستخدام منشئ المستندات، لذا فإن المراجعة الأولى هي مراجعة من نوع الإدراج.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// قم بإزالة تشغيل لإنشاء مراجعة من نوع الحذف.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// إضافة مراجعة جديدة يضعها في بداية مجموعة المراجعات.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// تظهر المراجعات المدرجة في نص المستند حتى قبل أن نقبل/نرفض المراجعة.
// سيؤدي رفض المراجعة إلى إزالة عقدها من النص. على العكس، فإن العقد التي تُشكل المراجعات تحذفها.
//أيضًا، نستمر في المستند حتى نقبل المراجعة.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// سيؤدي قبول مراجعة الحذف إلى إزالة العقدة الأصلية من نص الفقرة
// ثم قم بإزالة النسخة المعدلة للمجموعة نفسها.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// الآن قم بنقل العقدة لإنشاء نوع مراجعة متحرك.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// أصبحت النسخة المتحركة الآن في الفهرس 1. ارفض النسخة المتحركة للتخلص من محتوياتها.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
