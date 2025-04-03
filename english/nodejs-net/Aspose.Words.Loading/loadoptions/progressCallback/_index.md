---
title: LoadOptions.progressCallback property
linktitle: progressCallback property
articleTitle: progressCallback property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.progressCallback property. Called during loading a document and accepts data about loading progress."
type: docs
weight: 130
url: /nodejs-net/Aspose.Words.Loading/loadoptions/progressCallback/
---

## LoadOptions.progressCallback property

Called during loading a document and accepts data about loading progress.


```js
get progressCallback(): Aspose.Words.Loading.IDocumentLoadingCallback
```

### Remarks

[LoadFormat.Docx](../../../aspose.words/loadformat/#Docx), [LoadFormat.FlatOpc](../../../aspose.words/loadformat/#FlatOpc), [LoadFormat.Docm](../../../aspose.words/loadformat/#Docm), [LoadFormat.Dotm](../../../aspose.words/loadformat/#Dotm), [LoadFormat.Dotx](../../../aspose.words/loadformat/#Dotx), [LoadFormat.Markdown](../../../aspose.words/loadformat/#Markdown), [LoadFormat.Rtf](../../../aspose.words/loadformat/#Rtf), [LoadFormat.WordML](../../../aspose.words/loadformat/#WordML), [LoadFormat.Doc](../../../aspose.words/loadformat/#Doc), [LoadFormat.Dot](../../../aspose.words/loadformat/#Dot), [LoadFormat.Odt](../../../aspose.words/loadformat/#Odt), [LoadFormat.Ott](../../../aspose.words/loadformat/#Ott) formats supported.




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
* class [LoadOptions](../)

