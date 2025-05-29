---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PreserveEmptyLines di MarkdownLoadOptions migliora il caricamento del documento Markdown conservando le righe vuote per una migliore leggibilità.
type: docs
weight: 30
url: /it/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Ottiene o imposta un valore booleano che indica se preservare le righe vuote durante il caricamento di unMarkdown document. Il valore predefinito è`falso` .

Normalmente, le righe vuote tra gli elementi a livello di blocco in Markdown vengono ignorate. Anche le righe vuote all'inizio e alla fine del documento vengono ignorate. Questa opzione consente di importare tali righe vuote.

```csharp
public bool PreserveEmptyLines { get; set; }
```

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
