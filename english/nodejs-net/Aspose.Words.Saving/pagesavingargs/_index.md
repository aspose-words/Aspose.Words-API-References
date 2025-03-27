---
title: PageSavingArgs class
linktitle: PageSavingArgs class
articleTitle: PageSavingArgs class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PageSavingArgs class. Provides data for the [IPageSavingCallback.pageSaving()](../ipagesavingcallback/pageSaving/#pagesavingargs) event"
type: docs
weight: 560
url: /nodejs-net/Aspose.Words.Saving/pagesavingargs/
---

## PageSavingArgs class

Provides data for the [IPageSavingCallback.pageSaving()](../ipagesavingcallback/pageSaving/#pagesavingargs) event.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PageSavingArgs()](./PageSavingArgs/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [keepPageStreamOpen](./keepPageStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [pageFileName](./pageFileName/) | Gets or sets the file name where the document page will be saved to. |
| [pageIndex](./pageIndex/) | Current page index. |

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

