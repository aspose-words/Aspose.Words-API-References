---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words för .NET
description: Aspose.Words.Layout.PageLayoutEvent uppräkning. En händelsekod som uppstår under byggandet och renderingen av sidlayoutmodeller i C#.
type: docs
weight: 3370
url: /sv/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

En händelsekod som uppstår under byggandet och renderingen av sidlayoutmodeller.

Sidlayoutmodellen är byggd i två steg. Först, "konverteringssteg", det här är när sidlayout drar dokumentinnehåll och skapar objektgraf. För det andra, "reflow step", det här är när strukturer delas, slås samman och arrangeras till sidor.

Beroende på åtgärden som utlöste byggandet, kan sidlayoutmodellen eventuellt renderas ytterligare till ett fast sidformat. Till exempel kräver inte beräkning av antalet sidor i dokumentet eller uppdatering av fält rendering, medan export till Pdf gör det.

```csharp
public enum PageLayoutEvent
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Standardvärde |
| WatchDog | `1` | Motsvarar en kontrollpunkt i kod som ofta besöks och som är lämplig att avbryta processen. |
| BuildStarted | `2` | Byggandet av sidlayouten har påbörjats. Avfyrade en gång. Detta är den första händelsen som inträffar när[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heter. |
| BuildFinished | `3` | Bygget av sidlayouten har slutförts. Avfyrade en gång. Detta är den sista händelsen som inträffar när[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heter. |
| ConversionStarted | `4` | Konvertering av dokumentmodell till sidlayout har påbörjats. Avfyrade en gång. Detta inträffar när layoutmodellen börjar hämta dokumentinnehåll. |
| ConversionFinished | `5` | Konverteringen av dokumentmodell till sidlayout har slutförts. Avfyrades en gång. Detta inträffar när layoutmodellen slutar hämta dokumentinnehåll. |
| ReflowStarted | `6` | Omflödet av sidlayouten har startat. Avfyrades en gång. Detta inträffar när layoutmodellen börjar återflöda dokumentinnehållet. |
| ReflowFinished | `7` | Omflödet av sidlayouten har slutförts. Avfyrades en gång. Detta inträffar när layoutmodellen slutar flöda om dokumentinnehåll. |
| PartReflowStarted | `8` | Återflödet av sidan har startat. Observera att sidan kan återflödas flera gånger och att återflödet kan starta om innan det är klart. |
| PartReflowFinished | `9` | Återflödet av sidan har slutförts. Observera att sidan kan flöda om flera gånger och att återflödet kan starta om innan det är klart. |
| PartRenderingStarted | `10` | Renderingen av sidan har startat. Detta aktiveras en gång per sida. |
| PartRenderingFinished | `11` | Renderingen av sidan har slutförts. Detta aktiveras en gång per sida. |

## Exempel

Visar hur man spårar layoutändringar med en layoutåteruppringning.

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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
