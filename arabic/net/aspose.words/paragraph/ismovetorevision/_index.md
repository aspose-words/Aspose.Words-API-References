---
title: Paragraph.IsMoveToRevision
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. عوائد حقيقي إذا تم نقل هذا الكائن إدراجه في Microsoft Word أثناء تمكين تعقب التغيير.
type: docs
weight: 140
url: /ar/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير.

```csharp
public bool IsMoveToRevision { get; }
```

### أمثلة

يوضح كيفية التحقق مما إذا كانت الفقرة عبارة عن مراجعة للحركة.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// يحتوي هذا المستند على مراجعات "نقل" ، والتي تظهر عندما نبرز النص بالمؤشر ،
// ثم اسحبه لنقله إلى موقع آخر
// أثناء تتبع المراجعات في Microsoft Word عبر "مراجعة" - >; "تعقب التغيرات".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// نقل المراجعات تتكون من أزواج من المراجعات "الانتقال من" و "الانتقال إلى". 
// هذه المراجعات هي تغييرات محتملة على المستند يمكننا إما قبولها أو رفضها.
// قبل أن نقبل / نرفض مراجعة النقل ، المستند
// يجب أن يتتبع كلاً من وجهات المغادرة والوصول للنص.
// تحدد الفقرتان الثانية والرابعة أحد هذه المراجعة ، وبالتالي فإن كلاهما لهما نفس المحتويات.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// مراجعة "الانتقال من" هي الفقرة التي سحبنا النص منها.
// إذا قبلنا المراجعة ، ستختفي هذه الفقرة ،
// والآخر سيبقى ولن يكون مراجعة.
Assert.True(paragraphs[1].IsMoveFromRevision);

// مراجعة "الانتقال إلى" هي الفقرة التي سحبنا النص إليها.
// إذا رفضنا المراجعة ، فستختفي هذه الفقرة بدلاً من ذلك ، وستبقى الأخرى.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


