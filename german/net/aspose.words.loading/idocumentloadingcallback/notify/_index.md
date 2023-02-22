---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words für .NET-API-Referenz
description: IDocumentLoadingCallback methode. Dies wird aufgerufen um über den Ladefortschritt des Dokuments zu informieren.
type: docs
weight: 10
url: /de/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Dies wird aufgerufen, um über den Ladefortschritt des Dokuments zu informieren.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | DocumentLoadingArgs | Ein Argument der Veranstaltung. |

### Bemerkungen

Die primäre Verwendung dieser Schnittstelle besteht darin, dem Anwendungscode zu ermöglichen, den Fortschrittsstatus abzurufen und den Ladevorgang abzubrechen.

Eine Ausnahme sollte vom Fortschritts-Callback für den Abbruch geworfen und im Consumer-Code abgefangen werden.

### Beispiele

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

```csharp
[Test]
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
/// Brechen Sie das Laden eines Dokuments nach "MaxDuration" Sekunden ab.
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
    /// <param name="args">Lade Argumente.</param>
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
    /// Maximal erlaubte Dauer in Sek.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Siehe auch

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* namensraum [Aspose.Words.Loading](../../idocumentloadingcallback/)
* Montage [Aspose.Words](../../../)


