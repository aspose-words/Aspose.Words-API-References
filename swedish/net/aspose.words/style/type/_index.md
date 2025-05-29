---
title: Style.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Stiltyp för att enkelt komma åt och anpassa stycke- eller teckenformat, vilket förbättrar ditt dokuments visuella attraktionskraft.
type: docs
weight: 200
url: /sv/net/aspose.words/style/type/
---
## Style.Type property

Hämtar formateringstypen (stycke eller tecken).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
