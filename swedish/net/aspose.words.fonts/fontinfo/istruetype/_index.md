---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words för .NET
description: Upptäck FontInfos IsTrueType-egenskap, som säkerställer att ditt teckensnitt är TrueType eller OpenType för överlägsen kvalitet – perfekt för skarpa och skalbara designer.
type: docs
weight: 50
url: /sv/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indikerar att det här teckensnittet är ett TrueType- eller OpenType-teckensnitt i motsats till ett raster- eller vektorteckensnitt. Standard är`sann` .

```csharp
public bool IsTrueType { get; set; }
```

## Exempel

Visar hur man skriver ut information om vilka teckensnitt som finns i ett dokument.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Skriv ut alla använda och oanvända teckensnitt i dokumentet.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Se även

* class [FontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
