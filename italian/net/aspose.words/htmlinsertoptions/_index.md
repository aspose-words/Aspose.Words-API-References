---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.HtmlInsertOptions per personalizzare l'inserimento HTML con il metodo InsertHtml, migliorando l'efficienza di elaborazione dei documenti.
type: docs
weight: 3570
url: /it/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Specifica le opzioni per il[`InsertHtml`](../documentbuilder/inserthtml/) metodo.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Utilizza le opzioni predefinite quando inserisci HTML. |
| UseBuilderFormatting | `1` | Utilizza il formato del carattere e del paragrafo specificato in[`DocumentBuilder`](../documentbuilder/) come formattazione di base per il testo inserito da HTML. |
| RemoveLastEmptyParagraph | `2` | Rimuovi il paragrafo vuoto che normalmente viene inserito dopo l'HTML che termina con un elemento a livello di blocco. |
| PreserveBlocks | `4` | Conserva le proprietà degli elementi a livello di blocco. |

## Esempi

Mostra come è possibile preservare meglio i bordi e i margini visualizzati.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// Imposta la nuova modalità di importazione degli elementi HTML a livello di blocco.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
