---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ParagraphCollection فصل. يوفر الوصول المكتوب إلى مجموعة منParagraph العقد في C#.
type: docs
weight: 4410
url: /ar/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

يوفر الوصول المكتوب إلى مجموعة من[`Paragraph`](../paragraph/) العقد.

لمعرفة المزيد، قم بزيارة[العمل مع الفقرات](https://docs.aspose.com/words/net/working-with-paragraphs/) مقالة توثيقية.

```csharp
public class ParagraphCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | يسترد أ[`Paragraph`](../paragraph/) في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | إضافة عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | إزالة كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | تحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | إدراج عقدة في المجموعة في الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | إزالة العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | نسخ كافة الفقرات من المجموعة إلى مجموعة جديدة من الفقرات. (2 methods) |

## أمثلة

يوضح كيفية التحقق مما إذا كانت الفقرة عبارة عن مراجعة منقولة.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// يحتوي هذا المستند على مراجعات "نقل"، والتي تظهر عندما نقوم بتظليل النص باستخدام المؤشر،
// ثم اسحبه لنقله إلى موقع آخر
// أثناء تتبع المراجعات في Microsoft Word عبر "المراجعة" -> "تعقب التغيرات".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // نقل المراجعات يتكون من أزواج من المراجعات "الانتقال من" و"الانتقال إلى".
// هذه المراجعات هي تغييرات محتملة على المستند والتي يمكننا إما قبولها أو رفضها.
// قبل أن نقبل/نرفض مراجعة النقل، المستند
// يجب أن يتتبع وجهات المغادرة والوصول للنص.
// تحدد الفقرة الثانية والرابعة مراجعة واحدة من هذا القبيل، وبالتالي فإن كلاهما لهما نفس المحتوى.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// مراجعة "الانتقال من" هي الفقرة التي سحبنا النص منها.
// إذا قبلنا المراجعة، ستختفي هذه الفقرة،
// والآخر سيبقى ولن يكون مراجعة.
Assert.True(paragraphs[1].IsMoveFromRevision);

// مراجعة "الانتقال إلى" هي الفقرة التي قمنا بسحب النص إليها.
// إذا رفضنا المراجعة، ستختفي هذه الفقرة وتبقى الأخرى.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
