---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words for .NET
description: Customize your document layout with Aspose.Words.Layout.IPageLayoutCallback interface. Enhance rendering with your own methods for optimal results.
type: docs
weight: 3760
url: /net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implement this interface if you want to have your own custom method called during build and rendering of page layout model.

```csharp
public interface IPageLayoutCallback
```

## Methods

| Name | Description |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | This is called to notify of layout build and rendering progress. |

## Remarks

The primary use for this interface is to allow application code to abort build process.

It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.

Note, however, that rendering results may not match what would be rendered for each page if process would have finished.

This technique may not work for every document or may fail completely.

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

* property [Callback](../layoutoptions/callback/)
* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
