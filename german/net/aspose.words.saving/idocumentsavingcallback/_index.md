---
title: IDocumentSavingCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Implementieren Sie diese Schnittstelle wenn Sie möchten dass Ihre eigene benutzerdefinierte Methode beim Speichern eines Dokuments aufgerufen wird.
type: docs
weight: 4890
url: /de/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie möchten, dass Ihre eigene benutzerdefinierte Methode beim Speichern eines Dokuments aufgerufen wird.

```csharp
public interface IDocumentSavingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify/)(DocumentSavingArgs) | Dies wird aufgerufen, um über den Fortschritt des Dokumentspeicherns zu informieren. |

### Beispiele

Zeigt, wie ein Dokument beim Speichern in HTML verwaltet wird.

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
/// Rückruf zum Speichern des Fortschritts. Brechen Sie das Speichern eines Dokuments nach den "MaxDuration"-Sekunden ab.
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
    /// <param name="args">Argumente speichern.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal erlaubte Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Zeigt, wie ein Dokument verwaltet wird, während es als docx gespeichert wird.

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
/// Rückruf zum Speichern des Fortschritts. Brechen Sie das Speichern eines Dokuments nach den "MaxDuration"-Sekunden ab.
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
    /// <param name="args">Argumente speichern.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal erlaubte Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Zeigt, wie ein Dokument verwaltet wird, während es in xamlflow gespeichert wird.

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
/// Rückruf zum Speichern des Fortschritts. Brechen Sie das Speichern eines Dokuments nach den "MaxDuration"-Sekunden ab.
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
    /// <param name="args">Argumente speichern.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal erlaubte Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
