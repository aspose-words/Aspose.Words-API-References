---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words for .NET
description: IDocumentLoadingCallback Notify method. This is called to notify of document loading progress in C#.
type: docs
weight: 10
url: /net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

This is called to notify of document loading progress.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | DocumentLoadingArgs | An argument of the event. |

## Remarks

The primary uses for this interface is to allow application code to obtain progress status and abort loading process.

An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* namespace [Aspose.Words.Loading](../../idocumentloadingcallback/)
* assembly [Aspose.Words](../../../)
