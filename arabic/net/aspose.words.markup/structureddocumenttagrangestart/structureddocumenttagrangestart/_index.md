---
title: StructuredDocumentTagRangeStart
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words لـ .NET
description: أنشئ مثيلًا جديدًا لـ StructuredDocumentTagRangeStart بسهولة. حسّن إدارة مستنداتك باستخدام هذا المُنشئ القوي للعلامات المنظمة.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/structureddocumenttagrangestart/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart constructor

يقوم بتهيئة مثيل جديد لـ**بداية نطاق علامة المستند المنظم** الصف.

```csharp
public StructuredDocumentTagRangeStart(DocumentBase doc, SdtType type)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | DocumentBase | وثيقة المالك. |
| type | SdtType | نوع عقدة SDT. |

## ملاحظات

يمكن إنشاء الأنواع التالية من SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTagRangeStart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
