---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.DocumentSavingArgs, die für die effiziente Handhabung von Dokumentspeicherereignissen in Ihren Anwendungen unerlässlich ist.
type: docs
weight: 5700
url: /de/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Ein Argument, das übergeben wurde an[`Notify`](../idocumentsavingcallback/notify/) .

Um mehr zu erfahren, besuchen Sie die[Speichern eines Dokuments](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public sealed class DocumentSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Geschätzter Gesamtfortschritt in Prozent. |

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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
