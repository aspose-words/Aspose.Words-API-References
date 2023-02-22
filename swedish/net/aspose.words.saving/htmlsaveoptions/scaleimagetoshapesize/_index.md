---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om bilder skalas av Aspose.Words till den gränsande formstorleken vid export till HTML MHTML eller EPUB. Standardvärdet ärSann .
type: docs
weight: 450
url: /sv/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Anger om bilder skalas av Aspose.Words till den gränsande formstorleken vid export till HTML, MHTML eller EPUB. Standardvärdet är`Sann` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### Anmärkningar

En bild i ett Microsoft Word-dokument är en form. Formen har en storlek och image har sin egen storlek. Storlekarna är inte direkt kopplade. Till exempel kan bilden vara 1024x786 pixlar, men formen som visar denna bild kan vara 400x300 punkter.

För att visa en bild i webbläsaren måste den skalas till formstorleken. `ScaleImageToShapeSize` egenskapen styr var skalningen av image sker: i Aspose.Words under export till HTML eller i webbläsaren när dokumentet visas.

När`ScaleImageToShapeSize` är`Sann` , skalas bilden av Aspose.Words med högkvalitativ skalning under export till HTML. När`ScaleImageToShapeSize` är`falsk`bilden matas ut med sin ursprungliga storlek och webbläsaren måste skala den.

I allmänhet gör webbläsare snabb skalning av dålig kvalitet. Som ett resultat får du normalt bättre visningskvalitet i webbläsaren och mindre filstorlek när`ScaleImageToShapeSize` är`Sann` , men bättre utskriftskvalitet och snabbare konvertering när`ScaleImageToShapeSize` är`falsk`.

### Exempel

Visar hur du inaktiverar skalningen av bilder till deras överordnade formdimensioner när du sparar till .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Infoga en form som innehåller en bild och gör sedan den formen betydligt mindre än bilden.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Att spara ett dokument som innehåller former med bilder till HTML skapar en bildfil i det lokala filsystemet
            // för varje sådan form. HTML-dokumentet kommer att använda <image> taggar för att länka till och visa dessa bilder.
            // När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att fastställa
            // om alla bilder som finns i former ska skalas till storleken på deras former.
            // Att ställa in "ScaleImageToShapeSize"-flaggan till "true" kommer att krympa varje bild
            // till storleken på formen som innehåller den, så att inga sparade bilder blir större än vad dokumentet kräver att de ska vara.
            // Att ställa in "ScaleImageToShapeSize"-flaggan till "false" kommer att bevara dessa bilders ursprungliga storlekar,
            // som kommer att ta upp mer utrymme i utbyte mot att bevara bildkvaliteten.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Se även

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


