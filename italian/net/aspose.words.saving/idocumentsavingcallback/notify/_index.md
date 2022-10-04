---
title: Notify
second_title: Aspose.Words per .NET API Reference
description: Viene chiamato per notificare lavanzamento del salvataggio del documento.
type: docs
weight: 10
url: /it/net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

Viene chiamato per notificare l'avanzamento del salvataggio del documento.

```csharp
public void Notify(DocumentSavingArgs args)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| args | DocumentSavingArgs | Un argomento dell'evento. |

### Osservazioni

L'uso principale di questa interfaccia è consentire al codice dell'applicazione di ottenere lo stato di avanzamento e interrompere il processo di salvataggio.

Un'eccezione dovrebbe essere generata dal callback di avanzamento per l'aborto e dovrebbe essere catturata nel codice del consumatore.

### Esempi

Mostra come gestire un documento durante il salvataggio in html.

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
/// Salvataggio della richiamata di avanzamento. Annulla il salvataggio di un documento dopo i secondi "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il salvataggio del documento.
    /// </summary>
    /// <nome parametro="args">Salvataggio argomenti.</param>
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

Mostra come gestire un documento durante il salvataggio in docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Sono supportati i seguenti formati: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Salvataggio della richiamata di avanzamento. Annulla il salvataggio di un documento dopo i secondi "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il salvataggio del documento.
    /// </summary>
    /// <nome parametro="args">Salvataggio argomenti.</param>
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
    private const double MaxDuration = 0.01d;
}
```

Mostra come gestire un documento durante il salvataggio in xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Sono supportati i seguenti formati: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Salvataggio della richiamata di avanzamento. Annulla il salvataggio di un documento dopo i secondi "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Metodo di callback chiamato durante il salvataggio del documento.
    /// </summary>
    /// <nome parametro="args">Salvataggio argomenti.</param>
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
    private const double MaxDuration = 0.01d;
}
```

### Guarda anche

* class [DocumentSavingArgs](../../documentsavingargs/)
* interface [IDocumentSavingCallback](../)
* spazio dei nomi [Aspose.Words.Saving](../../idocumentsavingcallback/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
