---
title: Interface IDocumentLoadingCallback
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Loading.IDocumentLoadingCallback gränssnitt. Implementera det här gränssnittet om du vill att din egen anpassade metod ska anropas när ett dokument laddas.
type: docs
weight: 3430
url: /sv/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Implementera det här gränssnittet om du vill att din egen anpassade metod ska anropas när ett dokument laddas.

```csharp
public interface IDocumentLoadingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(DocumentLoadingArgs) | Detta anropas för att meddela om dokumentets laddningsförlopp. |

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

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)


