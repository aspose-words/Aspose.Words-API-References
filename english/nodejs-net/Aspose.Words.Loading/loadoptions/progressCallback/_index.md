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

[LoadFormat.Docx](../../../Aspose.Words/loadformat/#Docx), [LoadFormat.FlatOpc](../../../Aspose.Words/loadformat/#FlatOpc), [LoadFormat.Docm](../../../Aspose.Words/loadformat/#Docm), [LoadFormat.Dotm](../../../Aspose.Words/loadformat/#Dotm), [LoadFormat.Dotx](../../../Aspose.Words/loadformat/#Dotx), [LoadFormat.Markdown](../../../Aspose.Words/loadformat/#Markdown), [LoadFormat.Rtf](../../../Aspose.Words/loadformat/#Rtf), [LoadFormat.WordML](../../../Aspose.Words/loadformat/#WordML), [LoadFormat.Doc](../../../Aspose.Words/loadformat/#Doc), [LoadFormat.Dot](../../../Aspose.Words/loadformat/#Dot), [LoadFormat.Odt](../../../Aspose.Words/loadformat/#Odt), [LoadFormat.Ott](../../../Aspose.Words/loadformat/#Ott) formats supported.




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

