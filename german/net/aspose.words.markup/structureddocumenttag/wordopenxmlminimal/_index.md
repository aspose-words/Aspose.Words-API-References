---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words für .NET
description: StructuredDocumentTag WordOpenXMLMinimal eigendom. Ruft eine Zeichenfolge ab die das im Knoten im enthaltene XML darstelltFlatOpc format. Im Gegensatz zuWordOpenXMLEigenschaft generiert diese Methode ein reduziertes Dokument das alle nicht inhaltsbezogenen Teile ausschließt in C#.
type: docs
weight: 310
url: /de/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Ruft eine Zeichenfolge ab, die das im Knoten im enthaltene XML darstelltFlatOpc format. Im Gegensatz zu[`WordOpenXML`](../wordopenxml/)-Eigenschaft generiert diese Methode ein reduziertes Dokument, das alle nicht inhaltsbezogenen Teile ausschließt.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Beispiele

Zeigt, wie mit Stilen für Inhaltssteuerelemente gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 – Ein Stilobjekt aus der Stilsammlung des Dokuments anwenden:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 – Einen Stil im Dokument namentlich referenzieren:
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

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
