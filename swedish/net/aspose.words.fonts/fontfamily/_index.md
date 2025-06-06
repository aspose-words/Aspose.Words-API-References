---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fonts.FontFamily-uppräkningen – din nyckel till att enkelt hantera olika typsnittsfamiljer för förbättrad dokumentstyling och formatering.
type: docs
weight: 3340
url: /sv/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Representerar typsnittsfamiljen.

```csharp
public enum FontFamily
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Anger ett generiskt efternamn. Detta namn används när information om ett teckensnitt inte finns eller inte spelar någon roll. Standardteckensnittet används. |
| Roman | `1` | Anger ett proportionellt teckensnitt med seriffer. Ett exempel är Times New Roman. |
| Swiss | `2` | Anger ett proportionellt teckensnitt utan seriffer. Ett exempel är Arial. |
| Modern | `3` | Anger ett monospace-teckensnitt med eller utan seriffer. Monospace-teckensnitt är vanligtvis moderna; exempel inkluderar Pica, Elite och Courier New. |
| Script | `4` | Anger ett teckensnitt som är utformat för att se ut som handstil; exempel inkluderar Script och Cursive. |
| Decorative | `5` | Anger ett nyhetstypsnitt. Ett exempel är fornengelsk. |

## Anmärkningar

En typsnittsfamilj är en uppsättning typsnitt med gemensamma egenskaper för linjebredd och serif.

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
