---
title: StructuredDocumentTag.Style
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Ottiene o imposta lo stile del tag del documento strutturato.
type: docs
weight: 260
url: /it/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Ottiene o imposta lo stile del tag del documento strutturato.

```csharp
public Style Style { get; set; }
```

### Osservazioni

SoloCharacter stile oParagraph è possibile impostare uno stile con uno stile di carattere collegato.

### Esempi

Mostra come utilizzare gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto di stile dalla raccolta di stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Fa riferimento a uno stile nel documento per nome:
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

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


