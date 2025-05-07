---
title: PageLayoutCallbackArgs class
linktitle: PageLayoutCallbackArgs class
articleTitle: PageLayoutCallbackArgs class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.PageLayoutCallbackArgs class. An argument passed into [IPageLayoutCallback.notify()](../ipagelayoutcallback/notify/#pagelayoutcallbackargs) To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article."
type: docs
weight: 80
url: /nodejs-net/aspose.words.layout/pagelayoutcallbackargs/
---

## PageLayoutCallbackArgs class

An argument passed into [IPageLayoutCallback.notify()](../ipagelayoutcallback/notify/#pagelayoutcallbackargs)
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets document. |
| [event](./event/) | Gets event. |
| [pageIndex](./pageIndex/) | Gets 0-based index of the page in the document this event relates to. Returns negative value if there is no associated page, or if page was removed during reflow. |

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

