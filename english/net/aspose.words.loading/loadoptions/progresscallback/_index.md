---
title: LoadOptions.ProgressCallback
linktitle: ProgressCallback
second_title: Aspose.Words for .NET API Reference
description: LoadOptions ProgressCallback property. Called during loading a document and accepts data about loading progress in C#.
type: docs
weight: 130
url: /net/aspose.words.loading/loadoptions/progresscallback/
---
## ProgressCallback property

Called during loading a document and accepts data about loading progress.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

## Remarks

Docx, FlatOpc, Docm, Dotm, Dotx, Markdown, Rtf, WordML, Doc, Dot, Odt, Ott formats supported.

## Examples

Shows how to notify the user if document loading exceeded expected loading time.

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

        // Handle loading duration issue.
    }
}

/// <summary>
/// Cancel a document loading after the "MaxDuration" seconds.
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
    /// Callback method which called during document loading.
    /// </summary>
    /// <param name="args">Loading arguments.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// Date and time when document loading is started.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### See Also

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)
