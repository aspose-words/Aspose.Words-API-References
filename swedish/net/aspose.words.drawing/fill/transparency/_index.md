---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words för .NET
description: Justera fyllnadstransparensen från 0,0 (ogenomskinlig) till 1,0 (klar) för anpassningsbara visuella effekter i dina designer. Förbättra ditt projekts estetik idag!
type: docs
weight: 200
url: /sv/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Hämtar eller ställer in graden av genomskinlighet för den angivna fyllningen som ett värde mellan 0,0 (ogenomskinlig) och 1,0 (klar).

```csharp
public double Transparency { get; set; }
```

## Anmärkningar

Denna egenskap är motsatsen till egenskap[`Opacity`](../opacity/).

## Exempel

Visar hur man konverterar tillbaka fyllningarna till heldragen fyllning.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Hämta Fill-objekt för teckensnittet för den första körningen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Kontrollera fyllningsegenskaperna för teckensnittet.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändra fyllningstyp till Helfärgad med enhetlig grön färg.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
