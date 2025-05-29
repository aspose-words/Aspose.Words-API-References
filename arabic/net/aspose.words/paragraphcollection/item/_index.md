---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول بسهولة إلى فقرات محددة باستخدام خاصية "مجموعة الفقرات". استرجع أي فقرة حسب الفهرس لإدارة نص سلسة.
type: docs
weight: 10
url: /ar/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

يسترجع[`Paragraph`](../../paragraph/) عند الفهرس المعطى.

```csharp
public Paragraph this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
