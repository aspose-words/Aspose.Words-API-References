---
title: IPageLayoutCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for NodeJs
description: "IPageLayoutCallback.notify method. This is called to notify of layout build and rendering progress."
type: docs
weight: 10
url: /nodejs-net/aspose.words.layout/ipagelayoutcallback/notify/
---

## notify(args) {#pagelayoutcallbackargs}

This is called to notify of layout build and rendering progress.


```js
notify(args: Aspose.Words.Layout.PageLayoutCallbackArgs)
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/) | An argument of the event. |

### Remarks

Exception when thrown by implementation aborts layout build process.




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
* class [IPageLayoutCallback](../)

