---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words för .NET
description: Upptäck hur du effektivt ställer in FillType-egenskapen och förbättrar din design med anpassningsbara fyllningsalternativ för bättre visuell effekt.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Hämtar en fyllningstyp.

```csharp
public FillType FillType { get; }
```

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

* enum [FillType](../../filltype/)
* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
