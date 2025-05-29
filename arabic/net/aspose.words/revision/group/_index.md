---
title: Revision.Group
linktitle: Group
articleTitle: Group
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية مجموعة المراجعة، واسترجع مجموعات المراجعة بسهولة، أو احصل على قيمة فارغة في حال عدم وجود أي مجموعة. بسّط إدارة بياناتك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words/revision/group/
---
## Revision.Group property

يحصل على مجموعة المراجعة. يُرجع`باطل` إذا لم تكن المراجعة تنتمي إلى أي مجموعة.

```csharp
public RevisionGroup Group { get; }
```

## ملاحظات

لا يوجد للمراجعة مجموعة إذا كان نوع المراجعة هوStyleDefinitionChange or إذا لم تعد المراجعة موجودة في سياق المستند (مقبولة/مرفوضة).

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

* class [RevisionGroup](../../revisiongroup/)
* class [Revision](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
