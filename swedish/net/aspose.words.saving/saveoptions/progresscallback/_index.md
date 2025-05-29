---
title: SaveOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: Aspose.Words för .NET
description: Förbättra din dokumentsparningsupplevelse med egenskapen SaveOptions ProgressCallback, som ger realtidsuppdateringar om sparningsförloppet för sömlösa arbetsflöden.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/saveoptions/progresscallback/
---
## SaveOptions.ProgressCallback property

Anropas när ett dokument sparas och accepterar data om sparningsförloppet.

```csharp
public IDocumentSavingCallback ProgressCallback { get; set; }
```

## Anmärkningar

Förlopp rapporteras när man sparar tillDocx ,FlatOpc , Docm ,Dotm ,Dotx , Doc ,Dot , Html ,Mhtml ,Epub , XamlFlow , ellerXamlFlowPack .

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

Visar hur man hanterar ett dokument när man sparar det i docx-format.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Följande format stöds: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
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
    private const double MaxDuration = 0.01d;
}
```

Visar hur man hanterar ett dokument medan man sparar till xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Följande format stöds: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
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
    private const double MaxDuration = 0.01d;
}
```

### Se även

* interface [IDocumentSavingCallback](../../idocumentsavingcallback/)
* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
