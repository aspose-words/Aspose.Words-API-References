---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTag WordOpenXMLMinimal, som tillhandahåller en ren XML-sträng i FlatOpc-format, exklusive icke-innehållselement för effektiviserad dokumentbehandling.
type: docs
weight: 310
url: /sv/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. Till skillnad från[`WordOpenXML`](../wordopenxml/) egenskapen genererar den här metoden ett avskalat dokument som exkluderar alla delar som inte är innehållsrelaterade.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Exempel

Visar hur man arbetar med stilar för innehållskontrollelement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att tillämpa en stil från dokumentet på en strukturerad dokumenttagg.
// 1 - Använd ett stilobjekt från dokumentets stilsamling:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referera till en stil i dokumentet med namn:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
