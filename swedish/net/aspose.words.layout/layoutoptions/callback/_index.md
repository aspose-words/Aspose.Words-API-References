---
title: LayoutOptions.Callback
linktitle: Callback
articleTitle: Callback
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LayoutOptions Callback för att enkelt hantera IPageLayoutCallback för förbättrad anpassning av sidlayout och användarupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words.layout/layoutoptions/callback/
---
## LayoutOptions.Callback property

Hämtar eller sätter[`IPageLayoutCallback`](../../ipagelayoutcallback/) implementering som används av sidlayoutmodellen.

```csharp
public IPageLayoutCallback Callback { get; set; }
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

* interface [IPageLayoutCallback](../../ipagelayoutcallback/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
