---
title: LoadOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: Aspose.Words per .NET
description: Scopri la proprietà ProgressCallback di LoadOptions per monitorare in modo efficiente l'avanzamento del caricamento dei documenti. Migliora le prestazioni e l'esperienza utente della tua app!
type: docs
weight: 130
url: /it/net/aspose.words.loading/loadoptions/progresscallback/
---
## LoadOptions.ProgressCallback property

Viene chiamato durante il caricamento di un documento e accetta dati sullo stato di avanzamento del caricamento.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

## Osservazioni

Docx ,FlatOpc ,Docm ,Dotm ,Dotx ,Markdown ,Rtf ,WordML ,Doc ,Dot ,Odt ,Ott formati supportati.

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

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
