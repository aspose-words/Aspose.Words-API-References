---
title: IDocumentSavingCallback
second_title: Aspose.Words för .NET API Referens
description: Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad när du sparar ett dokument.
type: docs
weight: 4890
url: /sv/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad när du sparar ett dokument.

```csharp
public interface IDocumentSavingCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify)(DocumentSavingArgs) | Detta anropas för att meddela om hur dokumentet sparas. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
