---
title: EstimatedProgress
second_title: Aspose.Words för .NET API Referens
description: Totalt uppskattat procentuellt framsteg.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/documentsavingargs/estimatedprogress/
---
## DocumentSavingArgs.EstimatedProgress property

Totalt uppskattat procentuellt framsteg.

```csharp
public double EstimatedProgress { get; }
```

### Exempel

Visar hur man hanterar ett dokument samtidigt som man sparar till html.

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
/// Sparar förlopp för återuppringning. Avbryt ett dokumentsparande efter "MaxDuration" sekunderna.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Återuppringningsmetod som anropades under dokumentsparandet.
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
    /// Datum och tid när dokumentsparandet startas.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sek.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Visar hur du hanterar ett dokument samtidigt som du sparar till docx.

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
/// Sparar förlopp för återuppringning. Avbryt ett dokumentsparande efter "MaxDuration" sekunderna.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Återuppringningsmetod som anropades under dokumentsparandet.
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
    /// Datum och tid när dokumentsparandet startas.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Visar hur du hanterar ett dokument samtidigt som du sparar till xamlflow.

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
/// Sparar förlopp för återuppringning. Avbryt ett dokumentsparande efter "MaxDuration" sekunderna.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// Ctr.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// Återuppringningsmetod som anropades under dokumentsparandet.
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
    /// Datum och tid när dokumentsparandet startas.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximal tillåten varaktighet i sek.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### Se även

* class [DocumentSavingArgs](../)
* namnutrymme [Aspose.Words.Saving](../../documentsavingargs/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
