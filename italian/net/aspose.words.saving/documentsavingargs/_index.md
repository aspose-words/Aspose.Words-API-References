---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.DocumentSavingArgs, essenziale per gestire in modo efficiente gli eventi di salvataggio dei documenti nelle tue applicazioni.
type: docs
weight: 5700
url: /it/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Un argomento passato in[`Notify`](../idocumentsavingcallback/notify/) .

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public sealed class DocumentSavingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Progresso percentuale complessivo stimato. |

## Esempi

Mostra come gestire un documento durante il salvataggio in formato HTML.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Sono supportati i seguenti formati: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Callback di avanzamento del salvataggio. Annulla il salvataggio di un documento dopo i secondi "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il salvataggio del documento.
    /// </summary>
    /// <param name="args">Salvataggio degli argomenti.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Data e ora di inizio del salvataggio del documento.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Durata massima consentita in sec.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
