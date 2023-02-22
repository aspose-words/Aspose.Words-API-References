---
title: StyleCollection.GetEnumerator
second_title: Aspose.Words för .NET API Referens
description: StyleCollection metod. Hämtar ett uppräkningsobjekt som kommer att räkna upp stilar i alfabetisk ordning efter deras namn.
type: docs
weight: 90
url: /sv/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Hämtar ett uppräkningsobjekt som kommer att räkna upp stilar i alfabetisk ordning efter deras namn.

```csharp
public IEnumerator<Style> GetEnumerator()
```

### Exempel

Visar hur du kommer åt ett dokuments stilsamling.

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

* class [Style](../../style/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../stylecollection/)
* hopsättning [Aspose.Words](../../../)


