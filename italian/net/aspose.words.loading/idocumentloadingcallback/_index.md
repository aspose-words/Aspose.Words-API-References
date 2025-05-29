---
title: IDocumentLoadingCallback Interface
linktitle: IDocumentLoadingCallback
articleTitle: IDocumentLoadingCallback
second_title: Aspose.Words per .NET
description: Personalizza il caricamento dei documenti con Aspose.Words.IDocumentLoadingCallback. Implementa il tuo metodo per un maggiore controllo e flessibilità nella gestione dei documenti.
type: docs
weight: 4080
url: /it/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Implementa questa interfaccia se vuoi che venga chiamato il tuo metodo personalizzato durante il caricamento di un documento.

```csharp
public interface IDocumentLoadingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(*[DocumentLoadingArgs](../documentloadingargs/)*) | Viene chiamato per notificare l'avanzamento del caricamento del documento. |

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
