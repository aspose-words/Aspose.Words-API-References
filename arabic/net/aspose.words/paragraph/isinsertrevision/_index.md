---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Paragraph IsInsertRevision في Word. تعرّف على كيفية تحديد النص المُدرج أثناء تتبع التغييرات لإدارة المستندات بكفاءة.
type: docs
weight: 110
url: /ar/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات.

```csharp
public bool IsInsertRevision { get; }
```

## أمثلة

يوضح كيفية العمل مع فقرات المراجعة.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// الفقرات أعلاه ليست تنقيحات.
// سيتم تسجيل الفقرات التي نضيفها بعد بدء تتبع المراجعة باعتبارها مراجعات "إدراج".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// سيتم تسجيل الفقرات التي نقوم بإزالتها بعد بدء تتبع المراجعات على أنها مراجعات "محذوفة".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// ستبقى هذه الفقرات قائمة حتى نقبل أو نرفض تعديل الحذف.
// قبول المراجعة سيؤدي إلى إزالة الفقرة نهائيًا،
// ورفض المراجعة سوف يتركها في المستند كما لو أننا لم نحذفها أبدًا.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// قبول المراجعة، ثم التحقق من اختفاء الفقرة.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
