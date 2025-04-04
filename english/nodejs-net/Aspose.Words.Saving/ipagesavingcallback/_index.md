---
title: IPageSavingCallback class
linktitle: IPageSavingCallback class
articleTitle: IPageSavingCallback class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.IPageSavingCallback class. Implement this interface if you want to control how Aspose.Words saves separate pages when  saving a document to fixed page formats."
type: docs
weight: 340
url: /nodejs-net/aspose.words.saving/ipagesavingcallback/
---

## IPageSavingCallback class

Implement this interface if you want to control how Aspose.Words saves separate pages when 
saving a document to fixed page formats.


### Methods

| Name | Description |
| --- | --- |
|[ pageSaving(args)](./pageSaving/#pagesavingargs) | Called when Aspose.Words saves a separate page to fixed page formats. |

### Examples

Shows how to use a callback to save a document to HTML page by page.

```js
test('PageFileNames', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  builder.writeln("Page 1.");
  builder.insertBreak(aw.BreakType.PageBreak);
  builder.writeln("Page 2.");
  builder.insertImage(base.imageDir + "Logo.jpg");
  builder.insertBreak(aw.BreakType.PageBreak);
  builder.writeln("Page 3.");

  // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we convert the document to HTML.
  let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();

  // We will save each page in this document to a separate HTML file in the local file system.
  // Set a callback that allows us to name each output HTML document.
  htmlFixedSaveOptions.pageSavingCallback = new CustomFileNamePageSavingCallback();

  doc.save(base.artifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

  string[] filePaths = Directory.GetFiles(base.artifactsDir).Where(
    s => s.StartsWith(base.artifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

  expect(filePaths.length).toEqual(3);
});


  /// <summary>
  /// Saves all pages to a file and directory specified within.
  /// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
  public void PageSaving(PageSavingArgs args)
  {
    string outFileName = `${base.artifactsDir}SavingCallback.PageFileNames.Page_${args.pageIndex}.html`;

      // Below are two ways of specifying where Aspose.Words will save each page of the document.
      // 1 -  Set a filename for the output page file:
    args.pageFileName = outFileName;

      // 2 -  Create a custom stream for the output page file:
    args.pageStream = new FileStream(outFileName, FileMode.create);

    expect(args.keepPageStreamOpen).toEqual(false);
  }
}
```

### See Also

* module [Aspose.Words.Saving](../)

