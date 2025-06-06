---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Markup.MarkupLevel, che definisce dove StructuredDocumentTags si inseriscono nell'albero dei documenti per un'organizzazione e un controllo migliorati.
type: docs
weight: 4670
url: /it/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Specifica il livello nell'albero del documento in cui si trova un particolare[`StructuredDocumentTag`](../structureddocumenttag/) può verificarsi.

```csharp
public enum MarkupLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Unknown | `0` | Specifica il valore sconosciuto o non valido. |
| Inline | `1` | L'elemento si trova a livello inline (ad esempio tra sequenze di testo). |
| Block | `2` | L'elemento si trova a livello di blocco (ad esempio tra tabelle e paragrafi). |
| Row | `3` | L'elemento si trova tra le righe di una tabella. |
| Cell | `4` | L'elemento si trova tra le celle di una riga. |

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

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
