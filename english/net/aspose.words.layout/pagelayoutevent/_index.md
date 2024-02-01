---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.PageLayoutEvent enum. A code of event raised during page layout model build and rendering in C#.
type: docs
weight: 3500
url: /net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

A code of event raised during page layout model build and rendering.

Page layout model is built in two steps. First, "conversion step", this is when page layout pulls document content and creates object graph. Second, "reflow step", this is when structures are split, merged and arranged into pages.

Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format. For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.

```csharp
public enum PageLayoutEvent
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Default value |
| WatchDog | `1` | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. |
| BuildStarted | `2` | Build of the page layout has started. Fired once. This is the first event which occurs when [`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) is called. |
| BuildFinished | `3` | Build of the page layout has finished. Fired once. This is the last event which occurs when [`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) is called. |
| ConversionStarted | `4` | Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content. |
| ConversionFinished | `5` | Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content. |
| ReflowStarted | `6` | Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content. |
| ReflowFinished | `7` | Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content. |
| PartReflowStarted | `8` | Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartReflowFinished | `9` | Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartRenderingStarted | `10` | Rendering of page has started. This is fired once per page. |
| PartRenderingFinished | `11` | Rendering of page has finished. This is fired once per page. |

## Examples

Shows how to track layout changes with a layout callback.

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// Notifies us when we save the document to a fixed page format
/// and renders a page that we perform a page reflow on to an image in the local file system.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
