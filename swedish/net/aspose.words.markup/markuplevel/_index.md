---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Markup.MarkupLevel, som definierar var StructuredDocumentTags passar in i ditt dokumentträd för förbättrad organisation och kontroll.
type: docs
weight: 4670
url: /sv/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Anger nivån i dokumentträdet där en viss[`StructuredDocumentTag`](../structureddocumenttag/) kan förekomma.

```csharp
public enum MarkupLevel
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unknown | `0` | Anger det okända eller ogiltiga värdet. |
| Inline | `1` | Elementet förekommer på inline-nivå (t.ex. bland textsekvenser). |
| Block | `2` | Elementet förekommer på blocknivå (t.ex. bland tabeller och stycken). |
| Row | `3` | Elementet förekommer bland rader i en tabell. |
| Cell | `4` | Elementet förekommer bland celler i rad. |

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

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
