---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Drawing.FillType för att förbättra dina ifyllningsbara objekt med mångsidiga fyllningstyper för förbättrad dokumentdesign.
type: docs
weight: 1280
url: /sv/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Anger fyllningstyp för ett ifyllbart objekt.

```csharp
public enum FillType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Solid | `1` | Helfyllning. |
| Patterned | `2` | Mönstrad fyllning. |
| Gradient | `3` | Gradientfyllning. |
| Textured | `4` | Texturerad fyllning. |
| Background | `5` | Fyllningen är densamma som bakgrunden. |
| Picture | `6` | Bildfyllning. |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
