---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Style Name fast egendom. Hämtar eller ställer in namnet på stilen i C#.
type: docs
weight: 120
url: /sv/net/aspose.words/style/name/
---
## Style.Name property

Hämtar eller ställer in namnet på stilen.

```csharp
public string Name { get; set; }
```

## Anmärkningar

Kan inte vara tom sträng.

Om det redan finns en stil med ett sådant namn i samlingen, kommer denna stil att åsidosätta den. Alla berörda noder kommer att referera till ny stil.

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

Visar hur man klona ett dokuments stil.

```csharp
Document doc = new Document();

// AddCopy-metoden skapar en kopia av den angivna stilen och
// genererar automatiskt ett nytt namn för stilen, till exempel "Rubrik 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Använd stilens "Name"-egenskap för att ändra stilens identifierande namn.
newStyle.Name = "My Heading 1";

// Vårt dokument har nu två identiska stilar med olika namn.
// Ändring av inställningar för en av stilarna påverkar inte den andra.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
