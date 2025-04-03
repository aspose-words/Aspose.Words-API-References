---
title: PageLayoutEvent enumeration
linktitle: PageLayoutEvent enumeration
articleTitle: PageLayoutEvent enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Layout.PageLayoutEvent enumeration. A code of event raised during page layout model build and rendering."
type: docs
weight: 90
url: /nodejs-net/aspose.words.layout/pagelayoutevent/
---

## PageLayoutEvent enumeration

A code of event raised during page layout model build and rendering.



Page layout model is built in two steps.
First, "conversion step", this is when page layout pulls document content and creates object graph.
Second, "reflow step", this is when structures are split, merged and arranged into pages.



Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format.
For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.




### Members

| Name | Description |
| --- | --- |
| None | Default value |
| WatchDog | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. |
| BuildStarted | Build of the page layout has started. Fired once. This is the first event which occurs when [Document.updatePageLayout()](../../aspose.words/document/updatePageLayout/#default) is called. |
| BuildFinished | Build of the page layout has finished. Fired once. This is the last event which occurs when [Document.updatePageLayout()](../../aspose.words/document/updatePageLayout/#default) is called. |
| ConversionStarted | Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content. |
| ConversionFinished | Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content. |
| ReflowStarted | Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content. |
| ReflowFinished | Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content. |
| PartReflowStarted | Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartReflowFinished | Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartRenderingStarted | Rendering of page has started. This is fired once per page. |
| PartRenderingFinished | Rendering of page has finished. This is fired once per page. |

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

