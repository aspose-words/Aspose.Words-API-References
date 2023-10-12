---
title: HeaderFooter.HeaderFooter
second_title: Aspose.Words لمراجع .NET API
description: HeaderFooter البناء. إنشاء رأس أو تذييل جديد من النوع المحدد.
type: docs
weight: 10
url: /ar/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

إنشاء رأس أو تذييل جديد من النوع المحدد.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| headerFooterType | HeaderFooterType | أ[`HeaderFooterType`](../headerfootertype/) value الذي يحدد نوع الرأس أو التذييل. |

### ملاحظات

متى[`HeaderFooter`](../) تم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس بعد جزءًا من المستند و[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإلحاق[`HeaderFooter`](../)إلى أ[`Section`](../../section/) يستخدمNode) ,Node) أو[`HeadersFooters`](../../section/headersfooters/) الممتلكات والأساليب[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* مساحة الاسم [Aspose.Words](../../headerfooter/)
* المجسم [Aspose.Words](../../../)


