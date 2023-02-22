---
title: ImageSaveOptions.PaperColor
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Hämtar eller ställer in bakgrundsfärgen papper för de genererade bilderna.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Hämtar eller ställer in bakgrundsfärgen (papper) för de genererade bilderna.

Standardvärdet ärWhite.

```csharp
public Color PaperColor { get; set; }
```

### Anmärkningar

När du renderar sidor i ett dokument som anger sin egen bakgrundsfärg, , kommer dokumentets bakgrundsfärg att åsidosätta färgen som anges av den här egenskapen.

### Exempel

Återger en sida i ett Word-dokument till en bild med transparent eller färgad bakgrund.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Ställ in egenskapen "PaperColor" till en transparent färg för att tillämpa en transparent
// bakgrund till dokumentet medan du renderar det till en bild.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Ställ in egenskapen "PaperColor" till en ogenomskinlig färg för att tillämpa den färgen
// som bakgrund för dokumentet när vi renderar det till en bild.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Se även

* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


