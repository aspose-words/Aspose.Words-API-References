---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words för .NET
description: Upptäck HtmlLoadOptions WebRequestTimeout-egenskap, som låter dig anpassa timeout-inställningar för optimal webbprestanda. Standardvärde: 100 sekunder.
type: docs
weight: 80
url: /sv/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Antalet millisekunder som ska väntas innan webbförfrågan går ut. Standardvärdet är 100000 millisekunder (100 sekunder).

```csharp
public int WebRequestTimeout { get; set; }
```

## Anmärkningar

Antalet millisekunder som Aspose.Words väntar på ett svar när externa resurser (bilder, stilark) som är länkade i HTML- och MHTML-dokument laddas.

## Exempel

Visar hur man ställer in en tidsgräns för webbförfrågningar när man laddar ett dokument med externa resurser länkade via URL:er.

```csharp
public void WebRequestTimeout()
{
    // Skapa ett nytt HtmlLoadOptions-objekt och verifiera dess timeout-tröskelvärde för en webbförfrågan.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // När man laddar ett HTML-dokument med resurser externt länkade via en webbadress,
    // Aspose.Words kommer att avbryta webbförfrågningar som inte hämtar resurserna inom denna tidsgräns, i millisekunder.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Ställ in en WarningCallback som registrerar alla varningar som uppstår under inläsningen.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Ladda ett sådant dokument och verifiera att en form med bilddata har skapats.
    // Den här länkade bilden kräver en webbförfrågan för att laddas, vilken måste slutföras inom vår tidsgräns.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Ange en orimlig tidsgräns och försök läsa in dokumentet igen.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // En webbförfrågan som inte lyckas hämta en bild inom tidsgränsen kommer fortfarande att producera en bild.
    // Bilden kommer dock att vara det röda 'x' som vanligtvis indikerar saknade bilder.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Vi kan också konfigurera en anpassad återuppringning för att hämta varningar från tidsfördröjda webbförfrågningar.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Lagrar alla varningar som uppstår under en dokumentinläsning i en lista.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Se även

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
