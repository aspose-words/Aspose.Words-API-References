---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Fyllningsfärg för att enkelt anpassa din designs förgrundsfärg med ett Färg-objekt, vilket förbättrar ditt projekts visuella attraktionskraft.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Hämtar eller ställer in ett Color-objekt som representerar förgrundsfärgen för fyllningen.

```csharp
public Color Color { get; set; }
```

## Anmärkningar

Den här egenskapen bevarar alfakomponenten iColor , till skillnad från[`ForeColor`](../forecolor/) egenskap, vilket återställer den till helt ogenomskinlig färg.

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
