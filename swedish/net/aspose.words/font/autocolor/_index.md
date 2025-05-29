---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AutoColor för teckensnitt, hämta aktuell textfärg (svart eller vit) för automatiska färgjusteringar. Optimera din design utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Returnerar den aktuellt beräknade färgen på texten (svart eller vit) som ska användas för 'autofärg'. Om färgen inte är 'auto' returneras[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Anmärkningar

När text har "automatisk färg" beräknas textens faktiska färg automatiskt så att den är läsbar mot bakgrundsfärgen. När du ändrar bakgrundsfärgen växlar textfärgen automatiskt till svart eller vit i MS Word för att maximera läsbarheten.

## Exempel

Visar hur man förbättrar läsbarheten genom att automatiskt välja textfärg baserat på bakgrundens ljusstyrka.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om en körnings Font-objekt inte anger textfärg, kommer det automatiskt
// välj antingen svart eller vit beroende på bakgrundsfärgens färg.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Standardfärgen för text är svart. Om bakgrundsfärgen är mörk blir svart text svår att se.
// För att lösa detta problem kommer egenskapen AutoColor att visa denna text i vitt.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Om vi ändrar bakgrunden till en ljus färg blir svart mer
// lämpligare textfärg än vit så att den automatiska färgen visar den i svart.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
