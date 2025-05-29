---
title: PageLayoutCallbackArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words för .NET
description: Upptäck dokumentegenskapen PageLayoutCallbackArgs för att effektivt komma åt och hantera dina dokumentdata. Förbättra ditt arbetsflöde idag!
type: docs
weight: 10
url: /sv/net/aspose.words.layout/pagelayoutcallbackargs/document/
---
## PageLayoutCallbackArgs.Document property

Hämtar dokument.

```csharp
public Document Document { get; }
```

## Exempel

Visar hur man spårar layoutändringar med ett layoutåteranrop.

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
/// Meddelar oss när vi sparar dokumentet till ett fast sidformat
/// och renderar en sida som vi utför en sidflödesomflöde på till en bild i det lokala filsystemet.
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

### Se även

* class [Document](../../../aspose.words/document/)
* class [PageLayoutCallbackArgs](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
