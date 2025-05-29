---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Fyllnad för att förbättra din texts utseende med anpassningsbar fyllningsformatering för ett polerat och professionellt utseende.
type: docs
weight: 130
url: /sv/net/aspose.words/font/fill/
---
## Font.Fill property

Hämtar fyllningsformatering för[`Font`](../) .

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
