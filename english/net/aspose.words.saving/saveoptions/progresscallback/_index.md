---
title: SaveOptions.ProgressCallback
second_title: Aspose.Words for .NET API Reference
description: Called during saving a document and accepts data about saving progress.
type: docs
weight: 120
url: /net/aspose.words.saving/saveoptions/progresscallback/
---
## SaveOptions.ProgressCallback property

Called during saving a document and accepts data about saving progress.

```csharp
public IDocumentSavingCallback ProgressCallback { get; set; }
```

## Remarks

Progress is reported when saving to Docx, FlatOpc, Docm, Dotm, Dotx, Html, Mhtml, Epub, XamlFlow, or XamlFlowPack.

## Examples

Shows how to manage a document while saving to html.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Following formats are supported: Html, Mhtml, Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
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
    /// Callback method which called during document saving.
    /// </summary>
    /// <param name="args">Saving arguments.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date and time when document saving is started.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

Shows how to manage a document while saving to docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
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
    /// Callback method which called during document saving.
    /// </summary>
    /// <param name="args">Saving arguments.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date and time when document saving is started.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

Shows how to manage a document while saving to xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // Following formats are supported: XamlFlow, XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
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
    /// Callback method which called during document saving.
    /// </summary>
    /// <param name="args">Saving arguments.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date and time when document saving is started.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### See Also

* interface [IDocumentSavingCallback](../../idocumentsavingcallback/)
* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../saveoptions/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
