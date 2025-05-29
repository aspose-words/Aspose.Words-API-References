---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.ParagraphCollection للوصول بشكل سلس إلى عقد الفقرات المنظمة، مما يعزز معالجة المستندات والكفاءة في مشاريعك.
type: docs
weight: 5140
url: /ar/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

يوفر وصولاً مكتوبًا إلى مجموعة من[`Paragraph`](../paragraph/) العقد.

لمعرفة المزيد، قم بزيارة[العمل مع الفقرات](https://docs.aspose.com/words/net/working-with-paragraphs/) مقالة توثيقية.

```csharp
public class ParagraphCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | يسترجع[`Paragraph`](../paragraph/) عند الفهرس المعطى. (2 indexers) |

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
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | نسخ جميع الفقرات من المجموعة إلى مجموعة جديدة من الفقرات. (2 methods) |

## أمثلة

يوضح كيفية التحقق مما إذا كانت الفقرة عبارة عن مراجعة نقل.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// تحتوي هذه الوثيقة على مراجعات "النقل"، والتي تظهر عندما نقوم بتمييز النص باستخدام المؤشر،
// ثم اسحبه لنقله إلى مكان آخر
// أثناء تتبع المراجعات في Microsoft Word عبر "مراجعة" -> "تتبع التغييرات".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // تتكون مراجعات النقل من أزواج من مراجعات "النقل من" و"النقل إلى".
// هذه المراجعات هي تغييرات محتملة على المستند والتي يمكننا قبولها أو رفضها.
// قبل أن نقبل/نرفض مراجعة النقل، يجب أن تكون الوثيقة
// يجب أن يتتبع كل من وجهات المغادرة والوصول للنص.
// تحدد الفقرة الثانية والرابعة مثل هذه المراجعة، وبالتالي فإن كليهما لهما نفس المحتوى.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// إن المراجعة "الانتقال من" هي الفقرة التي قمنا بسحب النص منها.
// إذا قبلنا المراجعة، سوف تختفي هذه الفقرة،
// والآخر سيبقى ولن يكون مراجعة بعد الآن.
Assert.True(paragraphs[1].IsMoveFromRevision);

// إن المراجعة "نقل إلى" هي الفقرة التي قمنا بسحب النص إليها.
// إذا رفضنا المراجعة، فإن هذه الفقرة سوف تختفي بدلاً من ذلك، وستبقى الفقرة الأخرى.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
