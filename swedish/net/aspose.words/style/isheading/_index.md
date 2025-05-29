---
title: Style.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsHeading. Identifiera enkelt om en stil är en inbyggd rubrikstil, vilket förbättrar dokumentets struktur och läsbarhet.
type: docs
weight: 70
url: /sv/net/aspose.words/style/isheading/
---
## Style.IsHeading property

Sant när stilen är en av de inbyggda rubrikstilarna.

```csharp
public bool IsHeading { get; }
```

## Exempel

Visar hur man kommer åt ett dokuments stilsamling.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Räkna upp och lista alla stilar som ett dokument skapat med Aspose.Words innehåller som standard.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
