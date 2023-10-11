---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words per .NET API Reference
description: IDocumentLoadingCallback metodo. Viene richiamato per notificare lavanzamento del caricamento del documento.
type: docs
weight: 10
url: /it/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Viene richiamato per notificare l'avanzamento del caricamento del documento.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| args | DocumentLoadingArgs | Un argomento dell'evento. |

### Osservazioni

L'utilizzo principale di questa interfaccia è consentire al codice dell'applicazione di ottenere lo stato di avanzamento e interrompere il processo di caricamento.

Dovrebbe essere lanciata un'eccezione dal callback di avanzamento per l'aborto e dovrebbe essere inclusa nel codice del consumo.

### Esempi

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

        // Gestisce il problema relativo alla durata del caricamento.
    }
}

/// <summary>
/// Annulla il caricamento di un documento dopo i secondi "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il caricamento del documento.
    /// </summary>
    /// <param name="args">Caricamento degli argomenti.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Data e ora in cui viene avviato il caricamento del documento.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Durata massima consentita in sec.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Guarda anche

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* spazio dei nomi [Aspose.Words.Loading](../../idocumentloadingcallback/)
* assemblea [Aspose.Words](../../../)


