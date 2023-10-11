---
title: Class RevisionCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.RevisionCollection فصل. مجموعة منRevision الكائنات التي تمثل المراجعات في المستند.
type: docs
weight: 4770
url: /ar/net/aspose.words/revisioncollection/
---
## RevisionCollection class

مجموعة من[`Revision`](../revision/) الكائنات التي تمثل المراجعات في المستند.

لمعرفة المزيد، قم بزيارة[تتبع التغييرات في مستند](https://docs.aspose.com/words/net/track-changes-in-a-document/) مقالة توثيقية.

```csharp
public class RevisionCollection : IEnumerable<Revision>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/revisioncollection/count/) { get; } | إرجاع عدد المراجعات في المجموعة. |
| [Groups](../../aspose.words/revisioncollection/groups/) { get; } | مجموعة مجموعات المراجعة. |
| [Item](../../aspose.words/revisioncollection/item/) { get; } | إرجاع أ[`Revision`](../revision/) في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [AcceptAll](../../aspose.words/revisioncollection/acceptall/)() | يقبل كافة المراجعات في هذه المجموعة. |
| [GetEnumerator](../../aspose.words/revisioncollection/getenumerator/)() | يُرجع كائن العداد. |
| [RejectAll](../../aspose.words/revisioncollection/rejectall/)() | يرفض كافة المراجعات في هذه المجموعة. |

### ملاحظات

لا تقم بإنشاء مثيلات هذه الفئة مباشرة. استخدم ال[`Revisions`](../document/revisions/) الخاصية للحصول على المراجعات الموجودة في المستند.

### أمثلة

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

* class [Revision](../revision/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


