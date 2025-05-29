---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontInfo Name för att enkelt komma åt och använda teckensnittsnamn för förbättrad typografi i dina projekt.
type: docs
weight: 60
url: /sv/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Hämtar namnet på teckensnittet.

```csharp
public string Name { get; }
```

## Anmärkningar

Kan inte vara`null`Kan vara en tom sträng.

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
