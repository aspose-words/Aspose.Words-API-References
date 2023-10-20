---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words per .NET
description: Aspose.Words.HtmlInsertOptions enum. Specifica le opzioni perInsertHtml metodo in C#.
type: docs
weight: 3140
url: /it/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Specifica le opzioni per[`InsertHtml`](../documentbuilder/inserthtml/) metodo.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Utilizza le opzioni predefinite quando inserisci HTML. |
| UseBuilderFormatting | `1` | Utilizza la formattazione del carattere e del paragrafo specificata in[`DocumentBuilder`](../documentbuilder/) come formattazione di base per text inserito da HTML. |
| RemoveLastEmptyParagraph | `2` | Rimuovi il paragrafo vuoto che normalmente viene inserito dopo l'HTML che termina con un elemento a livello di blocco. |
| PreserveBlocks | `4` | Preserva le proprietà degli elementi a livello di blocco. |

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

// Imposta la nuova modalità di importazione di elementi HTML a livello di blocco.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
