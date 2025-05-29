---
title: FontPitch Enum
linktitle: FontPitch
articleTitle: FontPitch
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontPitch-enum, ett kraftfullt verktyg för att hantera teckensnitt och förbättra dokumentformatering i dina applikationer.
type: docs
weight: 3390
url: /sv/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Representerar teckensnittets breddgrad.

```csharp
public enum FontPitch
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Anger att ingen information finns tillgänglig om teckensnittets breddgrad. |
| Fixed | `1` | Anger att detta är ett teckensnitt med fast bredd. |
| Variable | `2` | Anger att detta är ett teckensnitt med proportionell bredd. |

## Anmärkningar

Bredvidden anger om teckensnittet har fast bredd, är proportionellt fördelat eller använder en standardinställning.

## Exempel

Visar hur man kommer åt och skriver ut information om varje teckensnitt i ett dokument.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt-namn är vanligtvis tomma.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Se även

* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
