---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat PageBreakBefore، وتحكم بسهولة في فواصل الصفحات قبل الفقرات لتحسين تنسيق المستند وسهولة قراءته.
type: docs
weight: 270
url: /ar/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

صحيح إذا تم فرض كسر الصفحة قبل الفقرة.

```csharp
public bool PageBreakBefore { get; set; }
```

## أمثلة

يوضح كيفية إنشاء فقرات تحتوي على فواصل الصفحات في البداية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اضبط هذا العلم على "true" لتطبيق فاصل الصفحة على بداية كل فقرة
// الذي سيقوم منشئ المستند بإنشائه ضمن تكوين ParagraphFormat هذا.
// لن تتلقى الفقرة الأولى فاصل الصفحة.
// اترك هذا العلم على "خطأ" لبدء كل فقرة جديدة في نفس الصفحة
// كما في السابق، بشرط وجود مساحة كافية.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
