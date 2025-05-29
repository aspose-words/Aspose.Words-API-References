---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words för .NET
description: Spåra dokumentinläsningen enkelt med metoden IDocumentLoadingCallback Notify. Förbättra användarupplevelsen med uppdateringar i realtid!
type: docs
weight: 10
url: /sv/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Detta anropas för att meddela om dokumentets inläsningsförlopp.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| args | DocumentLoadingArgs | Ett argument för händelsen. |

## Anmärkningar

Det här gränssnittet används huvudsakligen för att tillåta applikationskod att hämta förloppsstatus och avbryta laddningsprocessen.

Ett undantag bör genereras från progress-återanropet för abort och det bör fångas i konsumentkoden.

## Exempel

Visar hur man meddelar användaren om dokumentinläsningen överskrider den förväntade inläsningstiden.

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

        // Hantera problem med laddningstid.
    }
}

/// <summary>
/// Avbryt en dokumentinläsning efter "MaxDuration" sekunder.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// Centrum
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Återanropsmetod som anropades under dokumentinläsning.
    /// </summary>
    /// <param name="args">Laddar argument.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum och tid då dokumentinläsningen startade.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sekunder.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Se även

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
