---
title: IDocumentLoadingCallback.Notify
second_title: Aspose.Words för .NET API Referens
description: IDocumentLoadingCallback metod. Detta anropas för att meddela om dokumentets laddningsförlopp.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

Detta anropas för att meddela om dokumentets laddningsförlopp.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| args | DocumentLoadingArgs | Ett argument för händelsen. |

### Anmärkningar

De primära användningsområdena för detta gränssnitt är att tillåta applikationskod att erhålla förloppsstatus och avbryta laddningsprocessen.

Ett undantag bör kastas från förloppsåteruppringningen för abort och det bör fångas i konsumentkoden.

### Exempel

Visar hur man meddelar användaren om dokumentladdningen överskrider förväntad laddningstid.

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

        // Hantera problem med laddningstid.
    }
}

/// <summary>
/// Avbryt ett dokument som laddas efter "MaxDuration" sekunderna.
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
    /// Återuppringningsmetod som anropades under dokumentladdning.
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
    /// Datum och tid när dokumentladdningen startas.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sek.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### Se även

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* namnutrymme [Aspose.Words.Loading](../../idocumentloadingcallback/)
* hopsättning [Aspose.Words](../../../)


