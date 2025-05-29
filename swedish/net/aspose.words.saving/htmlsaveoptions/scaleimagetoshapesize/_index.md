---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words för .NET
description: Upptäck hur HtmlSaveOptions ScaleImageToShapeSize-egenskap optimerar bildskalning i Aspose.Words för HTML-, MHTML- eller EPUB-export. Förbättra dina dokument!
type: docs
weight: 470
url: /sv/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Anger om bilder skalas av Aspose.Words till den avgränsande formstorleken vid export till HTML, MHTML eller EPUB. Standardvärdet är`sann` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Anmärkningar

En bild i ett Microsoft Word-dokument är en form. Formen har en storlek och image har sin egen storlek. Storlekarna är inte direkt länkade. Till exempel kan bilden vara 1024x786 pixlar, men formen som visar bilden kan vara 400x300 punkter.

För att visa en bild i webbläsaren måste den skalas till formstorleken. Den`ScaleImageToShapeSize` egenskapen styr var skalningen av image sker: i Aspose.Words vid export till HTML eller i webbläsaren när dokumentet visas.

När`ScaleImageToShapeSize` är`sann` , bilden skalas av Aspose.Words med högkvalitativ skalning under export till HTML. När`ScaleImageToShapeSize` är`falsk`, bilden matas ut med sin ursprungliga storlek och webbläsaren måste skala den.

Generellt sett gör webbläsare snabb och dålig skalning. Som ett resultat får du normalt bättre visningskvalitet i webbläsaren och mindre filstorlek när`ScaleImageToShapeSize` är`sann` , men bättre utskriftskvalitet och snabbare konvertering när`ScaleImageToShapeSize` är`falsk`.

Förutom former som innehåller enskilda rasterbilder påverkar det här alternativet även gruppformer som består av rasterbilder. Om`ScaleImageToShapeSize` är`falsk` och en gruppform innehåller rasterbilder vars inneboende upplösning är högre än det värde som anges i[`ImageResolution`](../imageresolution/)Aspose.Words kommer att öka renderingsupplösningen för den gruppen. Detta gör att kvaliteten på grupperade högupplösta bilder kan bevaras bättre när de sparas till HTML.

## Exempel

Visar hur man inaktiverar skalning av bilder till deras överordnade formdimensioner när de sparas till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en form som innehåller en bild och gör sedan formen betydligt mindre än bilden.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Om man sparar ett dokument som innehåller former med bilder till HTML skapas en bildfil i det lokala filsystemet.
// för varje sådan form. HTML-dokumentet som utdata kommer att använda <image>-taggar för att länka till och visa dessa bilder.
// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att avgöra
// om alla bilder som finns inuti former ska skalas till storleken på deras former.
// Om flaggan "ScaleImageToShapeSize" sätts till "true" krymper du varje bild
// till storleken på formen som innehåller den, så att inga sparade bilder blir större än vad dokumentet kräver.
// Om flaggan "ScaleImageToShapeSize" ställs in på "false" bevaras bildernas ursprungliga storlekar.
// vilket tar upp mer utrymme i utbyte mot att bildkvaliteten bevaras.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Se även

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
