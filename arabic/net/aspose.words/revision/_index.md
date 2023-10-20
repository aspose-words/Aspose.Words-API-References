---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Revision فصل. يمثل مراجعة تغيير متعقب في عقدة أو نمط المستند. الاستخدامRevisionType للتحقق من نوع هذه المراجعة في C#.
type: docs
weight: 4760
url: /ar/net/aspose.words/revision/
---
## Revision class

يمثل مراجعة (تغيير متعقب) في عقدة أو نمط المستند. الاستخدام[`RevisionType`](./revisiontype/) للتحقق من نوع هذه المراجعة.

لمعرفة المزيد، قم بزيارة[تتبع التغييرات في مستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public class Revision
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | الحصول على مؤلف هذه المراجعة أو تعيينه. لا يمكن أن تكون سلسلة فارغة أو`باطل` . |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | الحصول على أو تعيين تاريخ/وقت هذه المراجعة. |
| [Group](../../aspose.words/revision/group/) { get; } | يحصل على مجموعة المراجعة. عائدات`باطل` إذا كانت المراجعة لا تنتمي إلى أي مجموعة. |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | الحصول على العقدة الأصلية المباشرة (المالك) لهذه المراجعة. ستعمل هذه الخاصية مع أي نوع مراجعة آخر غيرStyleDefinitionChange . |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | يحصل على النمط الأصلي المباشر (المالك) لهذه المراجعة. ستعمل هذه الخاصية فقط معStyleDefinitionChange نوع المراجعة. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | الحصول على نوع هذه المراجعة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | قبول هذه المراجعة. |
| [Reject](../../aspose.words/revision/reject/)() | رفض هذه المراجعة. |

## أمثلة

يوضح كيفية التعامل مع المراجعات في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// لا يعتبر التحرير العادي للمستند بمثابة مراجعة.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// لتسجيل تعديلاتنا كمراجعات، نحتاج إلى الإعلان عن المؤلف، ثم البدء في تتبعها.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// هذه العلامة تتوافق مع "المراجعة" -> "التتبع" -> خيار "تتبع التغييرات" في Microsoft Word.
// لا تؤثر طريقة "StartTrackRevisions" على قيمتها،
// والمستند يتتبع المراجعات برمجيًا على الرغم من أن قيمتها "خطأ".
// إذا فتحنا هذا المستند باستخدام Microsoft Word، فلن يتم تتبع المراجعات.
Assert.IsFalse(doc.TrackRevisions);

// لقد أضفنا نصًا باستخدام أداة إنشاء المستندات، لذا فإن المراجعة الأولى هي مراجعة من نوع الإدراج.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// قم بإزالة التشغيل لإنشاء مراجعة من نوع الحذف.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// إضافة مراجعة جديدة تضعها في بداية مجموعة المراجعة.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// تظهر المراجعات المُدرجة في نص المستند حتى قبل قبول/رفض المراجعة.
// سيؤدي رفض المراجعة إلى إزالة عقدها من النص. وعلى العكس من ذلك، فإن العقد التي تشكل المراجعات تحذف
// انتظر أيضًا في المستند حتى نقبل المراجعة.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// سيؤدي قبول مراجعة الحذف إلى إزالة العقدة الأصلية من نص الفقرة
// ثم قم بإزالة مراجعة المجموعة نفسها.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// الآن انقل العقدة لإنشاء نوع مراجعة متحرك.
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

// المراجعة المتحركة موجودة الآن في الفهرس 1. ارفض المراجعة لتجاهل محتوياتها.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
