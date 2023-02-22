---
title: StructuredDocumentTagRangeStart.RemoveAllChildren
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTagRangeStart طريقة. يزيل كافة العقد الموجودة بين عقدة بدء النطاق وعقدة نهاية النطاق.
type: docs
weight: 230
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/removeallchildren/
---
## StructuredDocumentTagRangeStart.RemoveAllChildren method

يزيل كافة العقد الموجودة بين عقدة بدء النطاق وعقدة نهاية النطاق.

```csharp
public void RemoveAllChildren()
```

### أمثلة

يوضح كيفية إنشاء / إزالة علامة مستند منظم ومحتوياته.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // يزيل علامة المستند المهيكلة النطاق ، لكنه يحتفظ بالمحتوى بالداخل.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    InsertStructuredDocumentTagRanges(doc, out rangeStart);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // يزيل علامة المستند المهيكلة النطاق والمحتوى بالداخل.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public void InsertStructuredDocumentTagRanges(Document doc, out StructuredDocumentTagRangeStart rangeStart)
{
    rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);
}
```

### أنظر أيضا

* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* المجسم [Aspose.Words](../../../)


