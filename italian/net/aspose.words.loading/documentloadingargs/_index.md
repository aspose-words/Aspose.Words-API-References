---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Loading.DocumentLoadingArgs per un caricamento efficiente dei documenti. Migliora il tuo flusso di lavoro con potenti argomenti di notifica.
type: docs
weight: 4040
url: /it/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

Un argomento passato in[`Notify`](../idocumentloadingcallback/notify/) .

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public sealed class DocumentLoadingArgs
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | Progresso percentuale complessivo stimato. |

## Esempi

Mostra come avvisare l'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

```csharp
public void ProgressCallback()
{
    LoadingProgressCallback progressCallback = new LoadingProgressCallback();

    LoadOptions loadOptions = new LoadOptions { ProgressCallback = progressCallback };

    try
    {
        Document doc = new Document(MyDir + "Big document.docx", loadOptions);
    }
    catch (OperationCanceledException exception)
    {
        Console.WriteLine(exception.Message);

        // Gestisci il problema della durata del caricamento.
    }
}

/// <summary>
/// Annulla il caricamento di un documento dopo i secondi "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Centro
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il caricamento del documento.
    /// </summary>
    /// <param name="args">Caricamento argomenti.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Data e ora di inizio del caricamento del documento.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Durata massima consentita in sec.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
