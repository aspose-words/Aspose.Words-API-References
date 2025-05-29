---
title: StructuredDocumentTag.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words für .NET
description: Entdecken Sie die StyleName-Eigenschaft von StructuredDocumentTag. Verwalten und passen Sie Stile für Ihre Dokumente einfach an, um Ordnung und Übersichtlichkeit zu verbessern.
type: docs
weight: 270
url: /de/net/aspose.words.markup/structureddocumenttag/stylename/
---
## StructuredDocumentTag.StyleName property

Ruft den Namen des Stils ab, der auf das strukturierte Dokument-Tag angewendet wird, oder legt ihn fest.

```csharp
public string StyleName { get; set; }
```

## Beispiele

Zeigt, wie mit Stilen für Inhaltssteuerelemente gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten finden Sie zwei Möglichkeiten, einen Stil aus dem Dokument auf ein strukturiertes Dokument-Tag anzuwenden.
// 1 – Wenden Sie ein Stilobjekt aus der Stilsammlung des Dokuments an:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Verweisen Sie im Dokument anhand des Namens auf einen Stil:
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
