---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.MarkupLevel opsomming. Gibt die Ebene im Dokumentbaum an auf der sich eine bestimmte befindetStructuredDocumentTag kann auftreten in C#.
type: docs
weight: 3980
url: /de/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Gibt die Ebene im Dokumentbaum an, auf der sich eine bestimmte befindet[`StructuredDocumentTag`](../structureddocumenttag/) kann auftreten.

```csharp
public enum MarkupLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unknown | `0` | Gibt den unbekannten oder ungültigen Wert an. |
| Inline | `1` | Das Element kommt auf der Inline-Ebene vor (z. B. zwischen Textläufen). |
| Block | `2` | Das Element kommt auf Blockebene vor (z. B. zwischen Tabellen und Absätzen). |
| Row | `3` | Das Element kommt zwischen Zeilen in einer Tabelle vor. |
| Cell | `4` | Das Element kommt zwischen Zellen in einer Zeile vor. |

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
