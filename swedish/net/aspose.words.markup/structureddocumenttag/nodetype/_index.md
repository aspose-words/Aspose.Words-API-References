---
title: StructuredDocumentTag.NodeType
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTag fast egendom. ReturnerarStructuredDocumentTag .
type: docs
weight: 220
url: /sv/net/aspose.words.markup/structureddocumenttag/nodetype/
---
## StructuredDocumentTag.NodeType property

ReturnerarStructuredDocumentTag .

```csharp
public override NodeType NodeType { get; }
```

### Exempel

Visar hur man arbetar med stilar för innehållskontrollelement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att tillämpa en stil från dokumentet på en strukturerad dokumenttagg.
// 1 - Använd ett stilobjekt från dokumentets stilsamling:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referera till en stil i dokumentet efter namn:
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttag/)
* hopsättning [Aspose.Words](../../../)


