---
title: RevisionCollection Class
linktitle: RevisionCollection
articleTitle: RevisionCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.RevisionCollection—قم بإدارة مراجعات المستندات بكفاءة باستخدام مجموعة قوية من كائنات المراجعة لتحرير سلس.
type: docs
weight: 5510
url: /ar/net/aspose.words/revisioncollection/
---
## RevisionCollection class

مجموعة من[`Revision`](../revision/) الكائنات التي تمثل المراجعات في المستند.

لمعرفة المزيد، قم بزيارة[تعقب التغييرات في المستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | يعيد عدد المراجعات في المجموعة. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | مجموعة من مجموعات المراجعة. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | يعيد[`Revision`](../revision/) عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Accept](../../aspose.words/revisioncollection/accept/)(*[IRevisionCriteria](../irevisioncriteria/)*) | يقبل المراجعات التي تتطابق مع المعايير المحددة. |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | يقبل جميع المراجعات في هذه المجموعة. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | يعيد كائن المعداد. |
| [Reject](../../aspose.words/revisioncollection/reject/)(*[IRevisionCriteria](../irevisioncriteria/)*) | يرفض المراجعات التي تتطابق مع المعايير المحددة. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | يرفض جميع المراجعات في هذه المجموعة. |

## ملاحظات

لا يمكنك إنشاء مثيلات لهذه الفئة مباشرةً. استخدم[`Revisions`](../document/revisions/) خاصية للحصول على المراجعات الموجودة في المستند.

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

* class [Revision](../revision/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
