---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen IsQuickStyle förbättrar din MS Word-upplevelse genom att visa upp stilar i Quick Style-galleriet för enkel åtkomst och förbättrat arbetsflöde.
type: docs
weight: 80
url: /sv/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Anger om den här stilen visas i snabbstilsgalleriet i MS Words användargränssnitt.

```csharp
public bool IsQuickStyle { get; set; }
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
