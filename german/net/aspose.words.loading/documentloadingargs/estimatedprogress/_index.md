---
title: DocumentLoadingArgs.EstimatedProgress
linktitle: EstimatedProgress
articleTitle: EstimatedProgress
second_title: Aspose.Words für .NET
description: Verfolgen Sie den Fortschritt mühelos mit der EstimatedProgress-Eigenschaft von DocumentLoadingArgs, die prozentuale Aktualisierungen in Echtzeit für mehr Effizienz bereitstellt.
type: docs
weight: 10
url: /de/net/aspose.words.loading/documentloadingargs/estimatedprogress/
---
## DocumentLoadingArgs.EstimatedProgress property

Geschätzter Gesamtfortschritt in Prozent.

```csharp
public double EstimatedProgress { get; }
```

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

* class [DocumentLoadingArgs](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
