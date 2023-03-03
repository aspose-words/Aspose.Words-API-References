---
title: PageLayoutCallbackArgs.Document
linktitle: Document
second_title: Aspose.Words for .NET API Reference
description: PageLayoutCallbackArgs property. Gets document in C#.
type: docs
weight: 10
url: /net/aspose.words.layout/pagelayoutcallbackargs/document/
---
## PageLayoutCallbackArgs.Document property

Gets document.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [PageLayoutCallbackArgs](../)
* namespace [Aspose.Words.Layout](../../pagelayoutcallbackargs/)
* assembly [Aspose.Words](../../../)
