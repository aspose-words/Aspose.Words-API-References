---
title: PageLayoutCallbackArgs Class
linktitle: PageLayoutCallbackArgs
articleTitle: PageLayoutCallbackArgs
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Layout.PageLayoutCallbackArgs för effektiv hantering av dokumentlayout. Förbättra ditt arbetsflöde med kraftfulla aviseringsfunktioner.
type: docs
weight: 3810
url: /sv/net/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class

Ett argument skickades in[`Notify`](../ipagelayoutcallback/notify/)

För att lära dig mer, besök[Konvertera till fast sidformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class PageLayoutCallbackArgs
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Document](../../aspose.words.layout/pagelayoutcallbackargs/document/) { get; } | Hämtar dokument. |
| [Event](../../aspose.words.layout/pagelayoutcallbackargs/event/) { get; } | Hämtar händelse. |
| [PageIndex](../../aspose.words.layout/pagelayoutcallbackargs/pageindex/) { get; } | Hämtar ett 0-baserat index för sidan i dokumentet som denna händelse relaterar till. Returnerar ett negativt värde om det inte finns någon associerad sida, eller om sidan togs bort under omflödet. |

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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
