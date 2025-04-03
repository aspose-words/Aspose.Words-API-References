---
title: IDocumentLoadingCallback class
linktitle: IDocumentLoadingCallback class
articleTitle: IDocumentLoadingCallback class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Loading.IDocumentLoadingCallback class. Implement this interface if you want to have your own custom method called during loading a document."
type: docs
weight: 80
url: /nodejs-net/aspose.words.loading/idocumentloadingcallback/
---

## IDocumentLoadingCallback class

Implement this interface if you want to have your own custom method called during loading a document.


### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#documentloadingargs) | This is called to notify of document loading progress. |

### Examples

Shows how to notify the user if document loading exceeded expected loading time.

```js
test.skip('ProgressCallback - TODO: WORDSNODEJS-122 - Add support of LoadOptions.ProgressCallback', () => {
    let progressCallback = new LoadingProgressCallback();

    let loadOptions = new aw.Loading.LoadOption();
    loadOptions.progressCallback = progressCallback;

    try
    {
      let doc = new aw.Document(base.myDir + "Big document.docx", loadOptions);
    }
    catch (err)
    {
      console.log(err);

      // Handle loading duration issue.
    }
  });

/*
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
      mLoadingStartedAt = Date.now();
    }

      /// <summary>
      /// Callback method which called during document loading.
      /// </summary>
      /// <param name="args">Loading arguments.</param>
    public void Notify(DocumentLoadingArgs args)
    {
      DateTime canceledAt = Date.now();
      double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

      if (ellapsedSeconds > MaxDuration)
        throw new OperationCanceledException(`EstimatedProgress = ${args.estimatedProgress}; CanceledAt = ${canceledAt}`);
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

* module [Aspose.Words.Loading](../)

