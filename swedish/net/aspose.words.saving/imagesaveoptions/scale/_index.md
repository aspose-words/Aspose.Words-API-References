---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words för .NET
description: Upptäck skalningsegenskapen ImageSaveOptions för att enkelt justera zoomfaktorn för dina bilder, vilket förbättrar kvaliteten och anpassningsmöjligheterna.
type: docs
weight: 150
url: /sv/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Hämtar eller ställer in zoomfaktorn för de genererade bilderna.

```csharp
public float Scale { get; set; }
```

## Anmärkningar

Standardvärdet är 1,0. Värdet måste vara större än 0.

## Exempel

Visar hur man renderar ett Office Math-objekt till en bildfil i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
// hur den renderar OfficeMath-noden till en bild.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Sätt egenskapen "Scale" till 5 för att rendera objektet till fem gånger sin ursprungliga storlek.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Visar hur man redigerar bilden medan Aspose.Words konverterar ett dokument till ett.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// redigera bilden medan sparoperationen renderar den.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
    // Båda är på en skala från 0 till 1 och är som standard på 0,5.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
    // Detta kommer att påverka bildens dimensioner.
    // Standardvärdet för dessa egenskaper är 96,0, för en upplösning på 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Vi kan skala bilden med den här egenskapen. Standardvärdet är 1.0, för en skalning på 100%.
    // Vi kan använda den här egenskapen för att neutralisera eventuella förändringar i bildens dimensioner som en ändring av upplösningen skulle orsaka.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
