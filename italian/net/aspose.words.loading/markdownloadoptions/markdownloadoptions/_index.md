---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words per .NET
description: Scopri il costruttore MarkdownLoadOptions per inizializzare facilmente le istanze di MarkdownLoadOptions per una migliore elaborazione e personalizzazione dei documenti.
type: docs
weight: 10
url: /it/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Inizializza una nuova istanza di[`MarkdownLoadOptions`](../) classe.

```csharp
public MarkdownLoadOptions()
```

## Osservazioni

Imposta automaticamente[`LoadFormat`](../../../aspose.words/loadformat/) AMarkdown .

## Esempi

Mostra come preservare la riga vuota durante il caricamento di un documento.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Guarda anche

* class [MarkdownLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
