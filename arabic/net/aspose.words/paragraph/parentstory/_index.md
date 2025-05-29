---
title: Paragraph.ParentStory
linktitle: ParentStory
articleTitle: ParentStory
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Paragraph ParentStory للوصول بسهولة إلى القصص على مستوى القسم الرئيسي، مما يعزز بنية مستندك باستخدام خيارات Body أو HeaderFooter.
type: docs
weight: 210
url: /ar/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

يسترد القصة على مستوى القسم الرئيسي التي يمكن[`Body`](../../body/) أو[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
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

* class [Story](../../story/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
