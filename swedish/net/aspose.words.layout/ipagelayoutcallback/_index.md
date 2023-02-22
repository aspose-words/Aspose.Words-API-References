---
title: Interface IPageLayoutCallback
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Layout.IPageLayoutCallback gränssnitt. Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad under byggandet och renderingen av sidlayoutmodellen.
type: docs
weight: 3110
url: /sv/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

Implementera detta gränssnitt om du vill ha din egen anpassade metod anropad under byggandet och renderingen av sidlayoutmodellen.

```csharp
public interface IPageLayoutCallback
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(PageLayoutCallbackArgs) | Detta anropas för att meddela om layoutens framsteg och rendering. |

### Anmärkningar

Den primära användningen av detta gränssnitt är att tillåta programkod att avbryta byggprocessen.

Det är möjligt att bygga en sidlayoutmodell för endast ett fåtal sidor i början av dokumentet och sedan avbryta processen och bara återge det som redan har byggts.

Observera dock att renderingsresultat kanske inte matchar det som skulle renderas för varje sida om processen skulle ha avslutats.

Denna teknik kanske inte fungerar för alla dokument eller kan misslyckas helt.

### Exempel

Visar hur man spårar layoutändringar med en layoutåteruppringning.

```csharp
[Test]
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
/// och renderar en sida som vi utför ett sidflöde på till en bild i det lokala filsystemet.
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


