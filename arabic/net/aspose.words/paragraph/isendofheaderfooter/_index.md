---
title: Paragraph.IsEndOfHeaderFooter
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة فيHeaderFooter قصة النص الرئيسي من أSection  كاذبة خلاف ذلك.
type: docs
weight: 70
url: /ar/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`HeaderFooter`](../../headerfooter/) (قصة النص الرئيسي) من أ[`Section`](../../section/) ; كاذبة خلاف ذلك.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

### أمثلة

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// قم بإنشاء رأس وألحق فقرة به. النص في تلك الفقرة
// سيظهر في أعلى كل صفحة من هذا القسم، فوق النص الأساسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// قم بإنشاء تذييل وإلحاق فقرة به. النص في تلك الفقرة
// سيظهر في أسفل كل صفحة من هذا القسم، أسفل النص الرئيسي.
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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


