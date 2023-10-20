---
title: LoadOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: Aspose.Words für .NET
description: LoadOptions ProgressCallback eigendom. Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten über den Ladefortschritt in C#.
type: docs
weight: 130
url: /de/net/aspose.words.loading/loadoptions/progresscallback/
---
## LoadOptions.ProgressCallback property

Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten über den Ladefortschritt.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

## Bemerkungen

Docx ,FlatOpc ,Docm ,Dotm ,Dotx ,Markdown ,Rtf ,WordML ,Doc ,Dot ,Odt ,Ott Unterstützte Formate.

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

        // Problem mit der Ladedauer behandeln.
    }
}

/// <summary>
/// Das Laden eines Dokuments nach den „MaxDuration“-Sekunden abbrechen.
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
    /// Callback-Methode, die beim Laden des Dokuments aufgerufen wurde.
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
    /// Datum und Uhrzeit, wann das Laden des Dokuments gestartet wird.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Maximal zulässige Dauer in Sekunden.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Siehe auch

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
