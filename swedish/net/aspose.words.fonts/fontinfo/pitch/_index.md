---
title: FontInfo.Pitch
second_title: Aspose.Words för .NET API Referens
description: FontInfo fast egendom. Tonhöjden indikerar om teckensnittet har fast tonhöjd proportionellt fördelat eller är beroende av en standardinställning.
type: docs
weight: 70
url: /sv/net/aspose.words.fonts/fontinfo/pitch/
---
## FontInfo.Pitch property

Tonhöjden indikerar om teckensnittet har fast tonhöjd, proportionellt fördelat eller är beroende av en standardinställning.

```csharp
public FontPitch Pitch { get; set; }
```

### Exempel

Visar hur du kommer åt och skriver ut detaljer för varje typsnitt i ett dokument.

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

* enum [FontPitch](../../fontpitch/)
* class [FontInfo](../)
* namnutrymme [Aspose.Words.Fonts](../../fontinfo/)
* hopsättning [Aspose.Words](../../../)


