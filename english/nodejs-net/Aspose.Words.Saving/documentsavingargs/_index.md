---
title: DocumentSavingArgs class
linktitle: DocumentSavingArgs class
articleTitle: DocumentSavingArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.DocumentSavingArgs class. An argument passed into Aspose.Words.Saving.IDocumentSavingCallback.Notify(Aspose.Words.Saving.DocumentSavingArgs)"
type: docs
weight: 120
url: /nodejs-net/aspose.words.saving/documentsavingargs/
---

## DocumentSavingArgs class

An argument passed into Aspose.Words.Saving.IDocumentSavingCallback.Notify(Aspose.Words.Saving.DocumentSavingArgs).
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [estimatedProgress](./estimatedProgress/) | Overall estimated percentage progress. |

### Examples

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

* module [Aspose.Words.Saving](../)

