---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words لـ .NET
description: Paragraph IsInsertRevision ملكية. إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات في C#.
type: docs
weight: 110
url: /ar/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

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

// الفقرات المذكورة أعلاه ليست مراجعات.
// الفقرات التي نضيفها بعد بدء تتبع المراجعة سيتم تسجيلها كمراجعات "إدراج".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// الفقرات التي نزيلها بعد بدء تتبع المراجعة سيتم تسجيلها كمراجعات "حذف".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// ستبقى هذه الفقرات حتى نقبل أو نرفض مراجعة الحذف.
// قبول المراجعة سيؤدي إلى إزالة الفقرة للأبد،
// ورفض المراجعة سيتركها في المستند كما لو أننا لم نحذفها أبدًا.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// اقبل المراجعة، ثم تحقق من انتهاء الفقرة.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
