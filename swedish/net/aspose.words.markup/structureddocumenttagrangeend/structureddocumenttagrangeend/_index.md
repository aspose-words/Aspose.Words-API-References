---
title: StructuredDocumentTagRangeEnd
linktitle: StructuredDocumentTagRangeEnd
articleTitle: StructuredDocumentTagRangeEnd
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn StructuredDocumentTagRangeEnd – initiera effektivt dokumenttaggintervall för förbättrad innehållshantering och sömlös integration.
type: docs
weight: 10
url: /sv/net/aspose.words.markup/structureddocumenttagrangeend/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd constructor

Initierar en ny instans av**Slut på intervallet för taggar för strukturerat dokument** klass.

```csharp
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| id | Int32 | Identifierare för motsvarande taggintervall för strukturerat dokument som startar. |

## Exempel

Visar hur man skapar/tar bort en strukturerad dokumenttagg och dess innehåll.

```csharp
public void SdtRangeExtendedMethods()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    StructuredDocumentTagRangeStart rangeStart = InsertStructuredDocumentTagRanges(doc);

    // Tar bort taggen för strukturerat dokument med varierande intervall, men behåller innehållet inuti.
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

    // Tar bort tagg och innehåll för strukturerat dokument med varierande intervall.
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

### Se även

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [StructuredDocumentTagRangeEnd](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
