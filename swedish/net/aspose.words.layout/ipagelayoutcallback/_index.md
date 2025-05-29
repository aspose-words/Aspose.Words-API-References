---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words för .NET
description: Anpassa din dokumentlayout med gränssnittet Aspose.Words.Layout.IPageLayoutCallback. Förbättra renderingen med dina egna metoder för optimala resultat.
type: docs
weight: 3760
url: /sv/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implementera det här gränssnittet om du vill att din egen anpassade metod ska anropas under byggandet och renderingen av sidlayoutmodellen.

```csharp
public interface IPageLayoutCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | Detta anropas för att meddela om layoutbyggande och renderingsförlopp. |

## Anmärkningar

Det primära användningen av det här gränssnittet är att tillåta applikationskod att avbryta byggprocessen.

Det är möjligt att bygga en sidlayoutmodell för endast ett fåtal sidor i början av dokumentet och sedan avbryta processen och bara rendera det som redan har byggts.

Observera dock att renderingsresultaten kanske inte matchar vad som skulle renderas för varje sida om processen hade avslutats.

Den här tekniken kanske inte fungerar för alla dokument eller så kan den misslyckas helt.

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

* property [Callback](../layoutoptions/callback/)
* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
