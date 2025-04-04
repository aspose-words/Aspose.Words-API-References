---
title: IDocumentLoadingCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for Node.js
description: "IDocumentLoadingCallback.notify method. This is called to notify of document loading progress."
type: docs
weight: 10
url: /nodejs-net/aspose.words.loading/idocumentloadingcallback/notify/
---

## notify(args) {#documentloadingargs}

This is called to notify of document loading progress.


```js
notify(args: Aspose.Words.Loading.DocumentLoadingArgs)
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../documentloadingargs/) | An argument of the event. |

### Remarks

The primary uses for this interface is to allow application code to obtain progress status and abort loading process.


An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.




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

* module [Aspose.Words.Loading](../../)
* class [IDocumentLoadingCallback](../)
* property [LoadOptions.progressCallback](../../loadoptions/progressCallback/)

