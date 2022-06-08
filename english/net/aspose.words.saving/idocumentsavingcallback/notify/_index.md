---
title: Notify
second_title: Aspose.Words for .NET API Reference
description: This is called to notify of document saving progress.
type: docs
weight: 10
url: /net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

This is called to notify of document saving progress.

```csharp
public void Notify(DocumentSavingArgs args)
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | DocumentSavingArgs | An argument of the event. |

## Remarks

The primary uses for this interface is to allow application code to obtain progress status and abort saving process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.

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

* class [DocumentSavingArgs](../../documentsavingargs)
* interface [IDocumentSavingCallback](../../idocumentsavingcallback)
* namespace [Aspose.Words.Saving](../../idocumentsavingcallback)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
