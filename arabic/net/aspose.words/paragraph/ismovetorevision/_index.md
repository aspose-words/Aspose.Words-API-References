---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsMoveToRevision في مايكروسوفت وورد! تعرّف على كيفية تتبع التغييرات وتحسين تجربة تحرير مستنداتك.
type: docs
weight: 140
url: /ar/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsMoveToRevision { get; }
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
