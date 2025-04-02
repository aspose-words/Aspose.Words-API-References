---
title: PageLayoutCallbackArgs.pageIndex property
linktitle: pageIndex property
articleTitle: pageIndex property
second_title: Aspose.Words for NodeJs
description: "PageLayoutCallbackArgs.pageIndex property. Gets 0-based index of the page in the document this event relates to"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Layout/pagelayoutcallbackargs/pageIndex/
---

## PageLayoutCallbackArgs.pageIndex property

Gets 0-based index of the page in the document this event relates to.
Returns negative value if there is no associated page, or if page was removed during reflow.


```js
get pageIndex(): number
```

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

* module [Aspose.Words.Layout](../../)
* class [PageLayoutCallbackArgs](../)

