---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsEndOfHeaderFooter للفقرات. حدّد بسهولة ما إذا كانت الفقرة الأخيرة في HeaderFooter، مما يُحسّن بنية المستند.
type: docs
weight: 70
url: /ar/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`HeaderFooter`](../../headerfooter/) (قصة النص الرئيسي) لـ[`Section`](../../section/) ؛ وإلا فسيكون خاطئًا.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

## أمثلة

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// أنشئ رأسًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أعلى كل صفحة من هذا القسم، فوق النص الرئيسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// أنشئ تذييلًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أسفل كل صفحة من هذا القسم، أسفل النص الرئيسي.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
