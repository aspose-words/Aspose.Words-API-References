---
title: DocumentLoadingArgs.EstimatedProgress
linktitle: EstimatedProgress
articleTitle: EstimatedProgress
second_title: Aspose.Words per .NET
description: Tieni traccia dei progressi senza sforzo con la proprietà EstimatedProgress di DocumentLoadingArgs, che fornisce aggiornamenti percentuali in tempo reale per una maggiore efficienza.
type: docs
weight: 10
url: /it/net/aspose.words.loading/documentloadingargs/estimatedprogress/
---
## DocumentLoadingArgs.EstimatedProgress property

Progresso percentuale complessivo stimato.

```csharp
public double EstimatedProgress { get; }
```

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

* class [DocumentLoadingArgs](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
