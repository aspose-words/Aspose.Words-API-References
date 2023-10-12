---
title: Paragraph.IsMoveToRevision
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. إرجاعحقيقي إذا تم نقل هذا الكائن إدراجه في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 140
url: /ar/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsMoveToRevision { get; }
```

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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


