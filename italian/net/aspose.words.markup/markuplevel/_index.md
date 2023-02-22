---
title: Enum MarkupLevel
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Markup.MarkupLevel enum. Specifica il livello nellalbero del documento in cui un particolareStructuredDocumentTag può verificarsi.
type: docs
weight: 3740
url: /it/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Specifica il livello nell'albero del documento in cui un particolare[`StructuredDocumentTag`](../structureddocumenttag/) può verificarsi.

```csharp
public enum MarkupLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unknown | `0` | Specifica il valore sconosciuto o non valido. |
| Inline | `1` | L'elemento si trova a livello inline (ad es. tra come sequenze di testo). |
| Block | `2` | L'elemento si trova a livello di blocco (es. tra tabelle e paragrafi). |
| Row | `3` | L'elemento si trova tra le righe di una tabella. |
| Cell | `4` | L'elemento si trova tra le celle di una riga. |

### Esempi

Mostra come lavorare con gli stili per gli elementi di controllo del contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per applicare uno stile dal documento a un tag di documento strutturato.
// 1 - Applica un oggetto di stile dalla raccolta di stili del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Fai riferimento a uno stile nel documento per nome:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)


