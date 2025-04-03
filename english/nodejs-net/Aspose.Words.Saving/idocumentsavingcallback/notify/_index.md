---
title: IDocumentSavingCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for NodeJs
description: "IDocumentSavingCallback.notify method. This is called to notify of document saving progress."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Saving/idocumentsavingcallback/notify/
---

## notify(args) {#documentsavingargs}

This is called to notify of document saving progress.


```js
notify(args: Aspose.Words.Saving.DocumentSavingArgs)
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [DocumentSavingArgs](../../documentsavingargs/) | An argument of the event. |

### Remarks

The primary uses for this interface is to allow application code to obtain progress status and abort saving process.


An exception should be threw from the progress callback for abortion and it should be caught in the consumer code.




### Examples

Shows how to manage a document while saving to xamlflow.

```js
test.each([SaveFormat.XamlFlow, "xamlflow",
  SaveFormat.XamlFlowPack, "xamlflowpack"])('ProgressCallback', (SaveFormat saveFormat, string ext) => {
  let doc = new aw.Document(base.myDir + "Big document.docx");

  // Following formats are supported: XamlFlow, XamlFlowPack.
  let saveOptions = new aw.Saving.XamlFlowSaveOptions(saveFormat)
  {
    ProgressCallback = new SavingProgressCallback()
  };

  var exception = Assert.Throws<OperationCanceledException>(() =>
    doc.save(base.artifactsDir + `XamlFlowSaveOptions.progressCallback.${ext}`, saveOptions));
  expect(exception?.Message.contains("EstimatedProgress")).toEqual(true);
});


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
    mSavingStartedAt = Date.now();
  }

    /// <summary>
    /// Callback method which called during document saving.
    /// </summary>
    /// <param name="args">Saving arguments.</param>
  public void Notify(DocumentSavingArgs args)
  {
    DateTime canceledAt = Date.now();
    double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
    if (ellapsedSeconds > MaxDuration)
      throw new OperationCanceledException(`EstimatedProgress = ${args.estimatedProgress}; CanceledAt = ${canceledAt}`);
  }

    /// <summary>
    /// Date and time when document saving is started.
    /// </summary>
  private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
  private const double MaxDuration = 0.01;
}
```

Shows how to manage a document while saving to html.

```js
test.skip.each([[aw.SaveFormat.Html, "html"],
  [aw.SaveFormat.Mhtml, "mhtml"],
  [aw.SaveFormat.Epub, "epub"]])('ProgressCallback - TODO: progressCallback not supported', (saveFormat, ext) => {
  let doc = new aw.Document(base.myDir + "Big document.docx");

  // Following formats are supported: Html, Mhtml, Epub.
  let saveOptions = new aw.Saving.HtmlSaveOptions(saveFormat);
  saveOptions.progressCallback = new SavingProgressCallback();

  expect(() =>
    doc.save(base.artifactsDir + `HtmlSaveOptions.progressCallback.${ext}`, saveOptions)).toThrow("OperationCanceledException");
});


/*
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
    mSavingStartedAt = Date.now();
  }

    /// <summary>
    /// Callback method which called during document saving.
    /// </summary>
    /// <param name="args">Saving arguments.</param>
  public void Notify(DocumentSavingArgs args)
  {
    DateTime canceledAt = Date.now();
    double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
    if (ellapsedSeconds > MaxDuration)
      throw new OperationCanceledException(`EstimatedProgress = ${args.estimatedProgress}; CanceledAt = ${canceledAt}`);
  }

    /// <summary>
    /// Date and time when document saving is started.
    /// </summary>
  private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// Maximum allowed duration in sec.
    /// </summary>
  private const double MaxDuration = 0.1;
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [IDocumentSavingCallback](../)

