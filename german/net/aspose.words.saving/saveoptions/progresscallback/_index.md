---
title: SaveOptions.ProgressCallback
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt.
type: docs
weight: 120
url: /de/net/aspose.words.saving/saveoptions/progresscallback/
---
## SaveOptions.ProgressCallback property

Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt.

```csharp
public IDocumentSavingCallback ProgressCallback { get; set; }
```

### Bemerkungen

Der Fortschritt wird beim Speichern gemeldetDocx ,FlatOpc , Docm ,Dotm ,Dotx , Doc ,Dot , Html ,Mhtml ,Epub , XamlFlow , oderXamlFlowPack .

### Beispiele

Zeigt, wie ein Dokument beim Speichern im HTML-Format verwaltet wird.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Folgende Formate werden unterstützt: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Rückruf zum Speicherfortschritt. Brechen Sie das Speichern eines Dokuments nach den „MaxDuration“-Sekunden ab.
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
    /// Callback-Methode, die beim Speichern des Dokuments aufgerufen wurde.
    /// </summary>
    /// <param name="args">Argumente werden gespeichert.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit, wann das Speichern des Dokuments gestartet wird.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sekunden.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Zeigt, wie ein Dokument beim Speichern im DOCX verwaltet wird.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Folgende Formate werden unterstützt: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Rückruf zum Speicherfortschritt. Brechen Sie das Speichern eines Dokuments nach den „MaxDuration“-Sekunden ab.
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
    /// Callback-Methode, die beim Speichern des Dokuments aufgerufen wurde.
    /// </summary>
    /// <param name="args">Argumente werden gespeichert.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit, wann das Speichern des Dokuments gestartet wird.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sekunden.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Zeigt, wie ein Dokument beim Speichern in xamlflow verwaltet wird.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Folgende Formate werden unterstützt: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Rückruf zum Speicherfortschritt. Brechen Sie das Speichern eines Dokuments nach den „MaxDuration“-Sekunden ab.
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
    /// Callback-Methode, die beim Speichern des Dokuments aufgerufen wurde.
    /// </summary>
    /// <param name="args">Argumente werden gespeichert.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit, wann das Speichern des Dokuments gestartet wird.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sekunden.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Siehe auch

* interface [IDocumentSavingCallback](../../idocumentsavingcallback/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


