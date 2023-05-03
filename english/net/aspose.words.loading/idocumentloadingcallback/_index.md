---
title: IDocumentLoadingCallback Interface
linktitle: IDocumentLoadingCallback
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Loading.IDocumentLoadingCallback interface. Implement this interface if you want to have your own custom method called during loading a document in C#.
type: docs
weight: 3570
url: /net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

Implement this interface if you want to have your own custom method called during loading a document.

```csharp
public interface IDocumentLoadingCallback
```

## Methods

| Name | Description |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(*[DocumentLoadingArgs](../documentloadingargs/)*) | This is called to notify of document loading progress. |

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

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
