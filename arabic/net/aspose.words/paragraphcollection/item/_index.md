---
title: ParagraphCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: ParagraphCollection ملكية. يسترد أParagraph في الفهرس المحدد.
type: docs
weight: 10
url: /ar/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

يسترد أ[`Paragraph`](../../paragraph/) في الفهرس المحدد.

```csharp
public Paragraph this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس في المجموعة. |

### ملاحظات

المؤشر قائم على الصفر.

الفهارس السالبة مسموح بها وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

إذا كان الفهرس سالبًا وقيمته المطلقة أكبر من عدد العناصر الموجودة في القائمة، فسيُرجع هذا مرجعًا فارغًا.

### أمثلة

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* مساحة الاسم [Aspose.Words](../../paragraphcollection/)
* المجسم [Aspose.Words](../../../)


