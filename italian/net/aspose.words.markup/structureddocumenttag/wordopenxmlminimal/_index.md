---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTag WordOpenXMLMinimal, che fornisce una stringa XML pulita in formato FlatOpc, escludendo gli elementi non di contenuto per un'elaborazione semplificata dei documenti.
type: docs
weight: 310
url: /it/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Ottiene una stringa che rappresenta l'XML contenuto nel nodo inFlatOpc format. A differenza del[`WordOpenXML`](../wordopenxml/) proprietà, questo metodo genera un documento ridotto che esclude tutte le parti non correlate al contenuto.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Esempi

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto stile dalla raccolta stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Riferimento a uno stile nel documento tramite il nome:
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

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
