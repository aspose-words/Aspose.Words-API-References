---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.DocumentSavingArgs, som är viktig för att effektivt hantera dokumentsparningshändelser i dina applikationer.
type: docs
weight: 5700
url: /sv/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

Ett argument skickades in[`Notify`](../idocumentsavingcallback/notify/) .

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public sealed class DocumentSavingArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | Totalt uppskattad procentuell framsteg. |

## Exempel

Visar hur man hanterar ett dokument när man sparar det till html.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Följande format stöds: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Återuppringning av sparningsförlopp. Avbryt en dokumentsparning efter "MaxDuration" sekunder.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Centrum
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Återanropsmetod som anropades när dokumentet sparades.
    /// </summary>
    /// <param name="args">Spara argument.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Datum och tid då dokumentsparandet startade.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sekunder.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
