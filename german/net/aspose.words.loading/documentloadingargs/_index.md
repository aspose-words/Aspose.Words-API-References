---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Loading.DocumentLoadingArgs für effizientes Laden von Dokumenten. Verbessern Sie Ihren Workflow mit leistungsstarken Benachrichtigungsargumenten.
type: docs
weight: 4040
url: /de/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

Ein Argument, das übergeben wurde an[`Notify`](../idocumentloadingcallback/notify/) .

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public sealed class DocumentLoadingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | Geschätzter Gesamtfortschritt in Prozent. |

## Beispiele

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

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

        // Problem der Ladedauer behandeln.
    }
}

/// <summary>
/// Brechen Sie das Laden eines Dokuments nach den „MaxDuration“-Sekunden ab.
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
    /// Rückrufmethode, die während des Ladens des Dokuments aufgerufen wird.
    /// </summary>
    /// <param name="args">Argumente werden geladen.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum und Uhrzeit des Beginns des Dokumentladevorgangs.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Siehe auch

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
