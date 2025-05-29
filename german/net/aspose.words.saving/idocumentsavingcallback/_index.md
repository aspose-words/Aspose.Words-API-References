---
title: IDocumentSavingCallback Interface
linktitle: IDocumentSavingCallback
articleTitle: IDocumentSavingCallback
second_title: Aspose.Words für .NET
description: Implementieren Sie die Schnittstelle Aspose.Words.Saving.IDocumentSavingCallback, um benutzerdefinierte Speichermethoden für Dokumente zu erstellen und so Ihre Dokumentenverwaltungslösungen zu verbessern.
type: docs
weight: 5900
url: /de/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

Implementieren Sie diese Schnittstelle, wenn Sie beim Speichern eines Dokuments Ihre eigene benutzerdefinierte Methode aufrufen möchten.

```csharp
public interface IDocumentSavingCallback
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify/)(*[DocumentSavingArgs](../documentsavingargs/)*) | Dies wird aufgerufen, um über den Fortschritt beim Speichern des Dokuments zu informieren. |

## Beispiele

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
/// Rückruf zum Speichern des Fortschritts. Bricht das Speichern eines Dokuments nach den "MaxDuration" Sekunden ab.
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
    /// Rückrufmethode, die während des Speicherns des Dokuments aufgerufen wird.
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
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Zeigt, wie ein Dokument beim Speichern im docx-Format verwaltet wird.

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
/// Rückruf zum Speichern des Fortschritts. Bricht das Speichern eines Dokuments nach den "MaxDuration" Sekunden ab.
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
    /// Rückrufmethode, die während des Speicherns des Dokuments aufgerufen wird.
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
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Zeigt, wie ein Dokument beim Speichern in XAMLFlow verwaltet wird.

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
/// Rückruf zum Speichern des Fortschritts. Bricht das Speichern eines Dokuments nach den "MaxDuration" Sekunden ab.
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
    /// Rückrufmethode, die während des Speicherns des Dokuments aufgerufen wird.
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
    /// Datum und Uhrzeit des Beginns der Dokumentspeicherung.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
