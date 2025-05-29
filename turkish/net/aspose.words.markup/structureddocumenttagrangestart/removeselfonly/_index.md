---
title: StructuredDocumentTagRangeStart.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: .NET için Aspose.Words
description: İçeriği korurken Yapılandırılmış Belge Etiketi aralığını zahmetsizce kaldırın. Belge yapınızı bugün RemoveSelfOnly yöntemiyle optimize edin!
type: docs
weight: 250
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/removeselfonly/
---
## StructuredDocumentTagRangeStart.RemoveSelfOnly method

Yapılandırılmış belge etiketinin bu aralık başlangıcını ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacının içinde tutar.

```csharp
public void RemoveSelfOnly()
```

## Örnekler

Yapılandırılmış belge etiketinin ve içeriğinin nasıl oluşturulacağını/kaldırılacağını gösterir.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // Aralıklı yapılandırılmış belge etiketini kaldırır, ancak içeriği içeride tutar.
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

    // Aralıklı yapılandırılmış belge etiketini ve içindeki içeriği kaldırır.
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

### Ayrıca bakınız

* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
