---
title: Paragraph.ParentStory
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. استرداد القصة الأصلية على مستوى القسم التي يمكن أن تكونBody أوHeaderFooter .
type: docs
weight: 210
url: /ar/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

استرداد القصة الأصلية على مستوى القسم التي يمكن أن تكون[`Body`](../../body/) أو[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

### أمثلة

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// إنشاء رأس وإلحاق فقرة به. النص في تلك الفقرة
// في أعلى كل صفحة من هذا القسم ، فوق النص الأساسي الرئيسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// إنشاء تذييل وإلحاق فقرة به. النص في تلك الفقرة
// في أسفل كل صفحة من هذا القسم ، أسفل النص الأساسي الرئيسي.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### أنظر أيضا

* class [Story](../../story/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


