---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words لـ .NET
description: Section ClearHeadersFooters طريقة. مسح رؤوس وتذييلات هذا القسم في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

مسح رؤوس وتذييلات هذا القسم.

```csharp
public void ClearHeadersFooters()
```

## ملاحظات

يتم مسح نص كافة الرؤوس والتذييلات، ولكن[`HeaderFooter`](../../headerfooter/) لا تتم إزالة الكائنات نفسها.

وهذا يجعل رؤوس وتذييلات هذا القسم مرتبطة برؤوس وتذييلات القسم السابق.

## أمثلة

يوضح كيفية مسح محتويات كافة الرؤوس والتذييلات في القسم.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// قم بإفراغ جميع الرؤوس والتذييلات في هذا القسم من جميع محتوياتها.
// ستظل الرؤوس والتذييلات نفسها موجودة ولكن لن يكون هناك أي شيء لعرضه.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
