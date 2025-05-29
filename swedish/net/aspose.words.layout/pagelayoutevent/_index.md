---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Layout.PageLayoutEvent-enumerationen – viktig för att optimera sidlayouthändelser under dokumentrendering och -byggande. Förbättra ditt arbetsflöde idag!
type: docs
weight: 3820
url: /sv/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

En händelsekod som genereras under byggandet och renderingen av en sidlayoutmodell.

Sidlayoutmodellen byggs i två steg. Först, "konverteringssteg", det är när sidlayouten hämtar dokumentinnehåll och skapar objektgraf. För det andra, "omflödessteg", det är när strukturer delas upp, sammanfogas och arrangeras till sidor.

Beroende på vilken åtgärd som utlöste byggandet kan sidlayoutmodellen renderas vidare till ett fast sidformat. Till exempel kräver inte beräkning av antalet sidor i dokumentet eller uppdatering av fält rendering, medan export till PDF gör det.

```csharp
public enum PageLayoutEvent
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Standardvärde |
| WatchDog | `1` | Motsvarar en kontrollpunkt i kod som ofta besöks och som är lämplig för att avbryta processen. |
| BuildStarted | `2` | Byggandet av sidlayouten har påbörjats. Utlöstes en gång. Detta är den första händelsen som inträffar när[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) kallas. |
| BuildFinished | `3` | Byggandet av sidlayouten har slutförts. Utlöstes en gång. Detta är den sista händelsen som inträffar när[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) kallas. |
| ConversionStarted | `4` | Konvertering av dokumentmodell till sidlayout har startat. Utlöstes en gång. Detta inträffar när layoutmodellen börjar hämta dokumentinnehåll. |
| ConversionFinished | `5` | Konverteringen av dokumentmodellen till sidlayouten har slutförts. Utlöstes en gång. Detta inträffar när layoutmodellen slutar hämta dokumentinnehåll. |
| ReflowStarted | `6` | Omflödet av sidlayouten har startats. Utlöstes en gång. Detta inträffar när layoutmodellen börjar omflödet av dokumentinnehållet. |
| ReflowFinished | `7` | Omflödet av sidlayouten har slutförts. Utlöstes en gång. Detta inträffar när layoutmodellen slutar omflödet av dokumentinnehållet. |
| PartReflowStarted | `8` | Sidans omflöde har startat. Observera att sidan kan omflödes flera gånger och att omflödet kan startas om innan det är klart. |
| PartReflowFinished | `9` | Sidans omflöde har slutförts. Observera att sidan kan omflödesas flera gånger och att omflödet kan startas om innan det är klart. |
| PartRenderingStarted | `10` | Rendering av sidan har startat. Detta utförs en gång per sida. |
| PartRenderingFinished | `11` | Renderingen av sidan är klar. Detta utförs en gång per sida. |

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
