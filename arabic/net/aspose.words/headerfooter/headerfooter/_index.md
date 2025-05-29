---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words لـ .NET
description: صمم رؤوسًا وتذييلات رائعة بسهولة باستخدام مُنشئنا البديهي. خصّص مظهر موقعك الإلكتروني بلمسة احترافية فريدة!
type: docs
weight: 10
url: /ar/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

ينشئ رأسًا أو تذييلًا جديدًا من النوع المحدد.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| headerFooterType | HeaderFooterType | أ[`HeaderFooterType`](../headerfootertype/)value التي تحدد نوع الرأس أو التذييل. |

## ملاحظات

متى[`HeaderFooter`](../) يتم إنشاؤه، فهو ينتمي إلى المستند المحدد، ولكنه ليس جزءًا من المستند بعد[`ParentNode`](../../node/parentnode/) يكون`باطل`.

لإضافة[`HeaderFooter`](../)الى[`Section`](../../section/) يستخدم[`InsertAfter`](../../compositenode/insertafter/) ،[`InsertBefore`](../../compositenode/insertbefore/) ، أو[`HeadersFooters`](../../section/headersfooters/) الممتلكات والطرق[`Add`](../../nodecollection/add/) ،[`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
