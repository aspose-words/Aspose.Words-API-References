---
title: Paragraph.IsDeleteRevision
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.
type: docs
weight: 40
url: /ar/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات.

```csharp
public bool IsDeleteRevision { get; }
```

### أمثلة

يوضح كيفية العمل مع فقرات المراجعة.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// الفقرات أعلاه ليست مراجعات.
// سيتم تسجيل الفقرات التي نضيفها بعد بدء تتبع المراجعة باعتبارها مراجعات "إدراج".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// سيتم تسجيل الفقرات التي نزيلها بعد بدء تتبع المراجعة باعتبارها مراجعات "حذف".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// ستبقى هذه الفقرات حتى نقبل أو نرفض مراجعة الحذف.
// سيؤدي قبول المراجعة إلى إزالة الفقرة نهائيًا ،
// وسيؤدي رفض المراجعة إلى تركها في المستند كما لو أننا لم نحذفها مطلقًا.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// قبول المراجعة ، ثم تحقق من اختفاء الفقرة.
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
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


