---
title: IPageLayoutCallback class
linktitle: IPageLayoutCallback class
articleTitle: IPageLayoutCallback class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Layout.IPageLayoutCallback class. Implement this interface if you want to have your own custom method called during build and rendering of page layout model."
type: docs
weight: 30
url: /nodejs-net/aspose.words.layout/ipagelayoutcallback/
---

## IPageLayoutCallback class

Implement this interface if you want to have your own custom method called during build and rendering of page layout model.


### Remarks

The primary use for this interface is to allow application code to abort build process.


It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.


Note, however, that rendering results may not match what would be rendered for each page if process would have finished.


This technique may not work for every document or may fail completely.




### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#pagelayoutcallbackargs) | This is called to notify of layout build and rendering progress. |

### Examples

Shows how to track layout changes with a layout callback.

```js
test('PageLayoutCallback', () => {
  let doc = new aw.Document();
  doc.builtInDocumentProperties.title = "My Document";

  let builder = new aw.DocumentBuilder(doc);
  builder.writeln("Hello world!");

  doc.layoutOptions.callback = new RenderPageLayoutCallback();
  doc.updatePageLayout();

  doc.save(base.artifactsDir + "Layout.PageLayoutCallback.pdf");
});


  /// <summary>
  /// Notifies us when we save the document to a fixed page format
  /// and renders a page that we perform a page reflow on to an image in the local file system.
  /// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
  public void Notify(PageLayoutCallbackArgs a)
  {
    switch (a.event)
    {
      case aw.Layout.PageLayoutEvent.PartReflowFinished:
        NotifyPartFinished(a);
        break;
      case aw.Layout.PageLayoutEvent.ConversionFinished:
        NotifyConversionFinished(a);
        break;
    }
  }

  private void NotifyPartFinished(PageLayoutCallbackArgs a)
  {
    console.log(`Part at page ${a.pageIndex + 1} reflow.`);
    RenderPage(a, a.pageIndex);
  }

  private void NotifyConversionFinished(PageLayoutCallbackArgs a)
  {
    console.log(`Document \"${a.document.builtInDocumentProperties.title}\" converted to page format.`);
  }

  private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
  {
    let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png) { PageSet = new aw.Saving.PageSet(pageIndex) };

      new FileStream(base.artifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
        FileMode.create))
      a.document.save(stream, saveOptions);
  }

  private int mNum;
}
```

### See Also

* module [Aspose.Words.Layout](../)
* property [LayoutOptions.callback](../layoutoptions/callback/)

