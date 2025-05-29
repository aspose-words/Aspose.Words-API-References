---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words für .NET
description: Verfolgen Sie den Ladevorgang von Dokumenten mühelos mit der IDocumentLoadingCallback-Notify-Methode. Verbessern Sie die Benutzerfreundlichkeit mit Echtzeit-Updates!
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
| args | DocumentLoadingArgs | Ein Argument des Ereignisses. |

## Bemerkungen

Die Hauptverwendung dieser Schnittstelle besteht darin, dem Anwendungscode zu ermöglichen, den Fortschrittsstatus abzurufen und den Ladevorgang abzubrechen.

Für den Abbruch sollte vom Fortschrittsrückruf eine Ausnahme ausgelöst und im Verbrauchercode abgefangen werden.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
