---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Markup.MarkupLevel, die definiert, wo StructuredDocumentTags in Ihren Dokumentbaum passen, um eine verbesserte Organisation und Kontrolle zu gewährleisten.
type: docs
weight: 4670
url: /de/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Gibt die Ebene im Dokumentbaum an, auf der ein bestimmter[`StructuredDocumentTag`](../structureddocumenttag/) kann vorkommen.

```csharp
public enum MarkupLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unknown | `0` | Gibt den unbekannten oder ungültigen Wert an. |
| Inline | `1` | Das Element kommt auf Inline-Ebene vor (z. B. zwischen Textzeilen). |
| Block | `2` | Das Element tritt auf Blockebene auf (z. B. zwischen Tabellen und Absätzen). |
| Row | `3` | Das Element kommt zwischen den Zeilen einer Tabelle vor. |
| Cell | `4` | Das Element tritt zwischen Zellen in einer Zeile auf. |

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
