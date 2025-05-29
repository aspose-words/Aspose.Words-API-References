---
title: DocumentLoadingArgs.EstimatedProgress
linktitle: EstimatedProgress
articleTitle: EstimatedProgress
second_title: Aspose.Words för .NET
description: Spåra framsteg enkelt med DocumentLoadingArgs EstimatedProgress-egenskap, som ger uppdateringar om procentandelar i realtid för ökad effektivitet.
type: docs
weight: 10
url: /sv/net/aspose.words.loading/documentloadingargs/estimatedprogress/
---
## DocumentLoadingArgs.EstimatedProgress property

Totalt uppskattad procentuell framsteg.

```csharp
public double EstimatedProgress { get; }
```

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

* class [DocumentLoadingArgs](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
