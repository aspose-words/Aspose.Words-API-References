---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Story AppendParagraph، وقم بإنشاء كائن فقرة وإضافته بسهولة باستخدام نص قابل للتخصيص لتحسين المستند بشكل سلس.
type: docs
weight: 60
url: /ar/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

طريقة اختصار لإنشاء[`Paragraph`](../../paragraph/) كائن يحتوي على نص اختياري ويضيفه إلى نهاية هذا الكائن.

```csharp
public Paragraph AppendParagraph(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | نص الفقرة. يمكن أن يكون`باطل` أو سلسلة فارغة. |

### قيمة الإرجاع

الفقرة الجديدة التي تم إنشاؤها وإضافتها.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
