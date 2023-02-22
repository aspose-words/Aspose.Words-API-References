---
title: Style.Styles
second_title: Aspose.Words för .NET API Referens
description: Style fast egendom. Får samlingen av stilar som denna stil tillhör.
type: docs
weight: 150
url: /sv/net/aspose.words/style/styles/
---
## Style.Styles property

Får samlingen av stilar som denna stil tillhör.

```csharp
public StyleCollection Styles { get; }
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

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../style/)
* hopsättning [Aspose.Words](../../../)


