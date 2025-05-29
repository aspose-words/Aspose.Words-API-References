---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words لـ .NET
description: اكتشف فقرات القصة. اطلع على مجموعة مختارة من الفقرات مباشرةً من قصتك، مما يُعزز سردك بمحتوى غني وجذاب.
type: docs
weight: 30
url: /ar/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

يحصل على مجموعة من الفقرات التي تعتبر أبناءً مباشرين للقصة.

```csharp
public ParagraphCollection Paragraphs { get; }
```

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

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
