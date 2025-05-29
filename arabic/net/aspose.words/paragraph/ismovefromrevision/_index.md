---
title: Paragraph.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsMoveFromRevision في مايكروسوفت وورد! تعرّف على كيفية استخدامها للإشارة إلى نقل أو حذف كائن أثناء تتبع التغييرات.
type: docs
weight: 130
url: /ar/net/aspose.words/paragraph/ismovefromrevision/
---
## Paragraph.IsMoveFromRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsMoveFromRevision { get; }
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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
