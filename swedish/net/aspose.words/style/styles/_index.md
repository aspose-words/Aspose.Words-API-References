---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: Aspose.Words för .NET
description: Style Styles fast egendom. Får samlingen av stilar som denna stil tillhör i C#.
type: docs
weight: 160
url: /sv/net/aspose.words/style/styles/
---
## Style.Styles property

Får samlingen av stilar som denna stil tillhör.

```csharp
public StyleCollection Styles { get; }
```

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
