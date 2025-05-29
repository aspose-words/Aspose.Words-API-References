---
title: StructuredDocumentTagRangeStart.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words لـ .NET
description: أزل نطاق علامات المستند الهيكلي بسهولة مع الحفاظ على المحتوى. حسّن بنية مستندك باستخدام طريقة RemoveSelfOnly اليوم!
type: docs
weight: 250
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/removeselfonly/
---
## StructuredDocumentTagRangeStart.RemoveSelfOnly method

يزيل عقدة بداية هذا النطاق وعقدة نهاية النطاق المناسبة لعلامة المستند المنظم، ولكنه يحتفظ بمحتواه داخل شجرة المستند.

```csharp
public void RemoveSelfOnly()
```

## أمثلة

يوضح كيفية إنشاء/إزالة علامة المستند المنظم ومحتواه.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // يقوم بإزالة علامة المستند المنظمة المحددة، لكنه يحتفظ بالمحتوى الموجود بداخله.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    rangeStart = InsertStructuredDocumentTagRanges(doc);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // يقوم بإزالة علامة المستند المنظمة والمحددة والمحتوى الموجود بداخلها.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public StructuredDocumentTagRangeStart InsertStructuredDocumentTagRanges(Document doc)
{
    StructuredDocumentTagRangeStart rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);

    return rangeStart;
}
```

### أنظر أيضا

* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
