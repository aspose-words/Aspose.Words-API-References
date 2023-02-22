---
title: ImageSaveOptions.UseGdiEmfRenderer
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör om GDI eller Aspose.Wordsmetafilrenderare ska användas när du sparar till EMF.
type: docs
weight: 180
url: /sv/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Hämtar eller ställer in ett värde som avgör om GDI+ eller Aspose.Words-metafilrenderare ska användas när du sparar till EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

### Anmärkningar

Om inställt på`Sann`GDI+ metafil-renderare används. Dvs innehåll skrivs till GDI+ graphics objekt och sparas till metafil.

Om inställt på`falsk` Aspose.Words metafil-renderare används. Dvs innehåll skrivs direkt till metafilformatet med Aspose.Words.

Har effekt endast när du sparar till EMF.

GDI+-sparande fungerar bara på .NET.

Standardvärdet är`Sann`.

### Exempel

Visar hur man väljer en renderare när man konverterar ett dokument till .emf.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // När vi sparar dokumentet som en EMF-bild kan vi skicka ett SaveOptions-objekt för att välja en renderare för bilden.
            // Om vi sätter "UseGdiEmfRenderer"-flaggan till "true", kommer Aspose.Words att använda GDI+-renderaren.
            // Om vi sätter "UseGdiEmfRenderer"-flaggan till "false", kommer Aspose.Words att använda sin egen metafil-renderare.
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // GDI+-renderaren skapar vanligtvis större filer.
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


