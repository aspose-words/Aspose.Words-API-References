---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words per .NET API Reference
description: IDocumentLoadingCallback metodo. Viene chiamato per notificare lavanzamento del caricamento del documento.
type: docs
weight: 10
url: /it/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Viene chiamato per notificare l'avanzamento del caricamento del documento.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| args | DocumentLoadingArgs | Un argomento dell'evento. |

### Osservazioni

L'uso principale di questa interfaccia è consentire al codice dell'applicazione di ottenere lo stato di avanzamento e interrompere il processo di caricamento.

Un'eccezione dovrebbe essere generata dal callback di avanzamento per l'aborto e dovrebbe essere catturata nel codice del consumatore.

### Esempi

Mostra come notificare all'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

```csharp
[Test]
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

        // Gestisce il problema della durata del caricamento.
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
    /// <nome parametro="args">Caricamento argomenti.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Data e ora di avvio del caricamento del documento.
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


