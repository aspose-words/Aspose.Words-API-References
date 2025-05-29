---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words per .NET
description: Monitora l'avanzamento del caricamento dei documenti senza sforzo con il metodo IDocumentLoadingCallback Notify. Migliora l'esperienza utente con aggiornamenti in tempo reale!
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

## Osservazioni

L'uso principale di questa interfaccia è consentire al codice dell'applicazione di ottenere lo stato di avanzamento e di annullare il processo di caricamento.

Dovrebbe essere generata un'eccezione dal callback di avanzamento per l'aborto e dovrebbe essere catturata nel codice del consumatore.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
