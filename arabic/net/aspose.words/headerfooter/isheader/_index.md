---
title: HeaderFooter.IsHeader
second_title: Aspose.Words لمراجع .NET API
description: HeaderFooter ملكية. صحيح إذا كان هذاHeaderFooter الكائن عبارة عن رأس.
type: docs
weight: 30
url: /ar/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

صحيح إذا كان هذا[`HeaderFooter`](../) الكائن عبارة عن رأس.

```csharp
public bool IsHeader { get; }
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

* class [HeaderFooter](../)
* مساحة الاسم [Aspose.Words](../../headerfooter/)
* المجسم [Aspose.Words](../../../)


