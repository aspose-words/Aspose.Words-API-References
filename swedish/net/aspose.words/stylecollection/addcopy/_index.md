---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words för .NET
description: Kopiera enkelt stilar med StyleCollection AddCopy-metoden. Förbättra ditt designarbetsflöde och effektivisera din stilhantering idag!
type: docs
weight: 70
url: /sv/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

Kopierar en stil till den här samlingen.

```csharp
public Style AddCopy(Style style)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| style | Style | Stil som ska kopieras. |

### Returvärde

Kopierad stil klar för användning.

## Anmärkningar

Stilen som ska kopieras kan tillhöra samma dokument såväl som ett annat dokument.

Länkad stil kopieras.

Den här metoden kopierar inte basstilar.

Om samlingen redan innehåller en stil med samma namn genereras det nya namnet automatiskt genom att lägga till suffixet "_number" som börjar från 0, t.ex. "Normal_0", "Rubrik 1_1" etc. Använd[`Name`](../../style/name/) inställare för att ändra namnet på den importerade stilen.

## Exempel

Visar hur man importerar en stil från ett dokument till ett annat.

```csharp
Document srcDoc = new Document();

// Skapa en anpassad stil för källdokumentet.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// Importera källdokumentets anpassade stil till destinationsdokumentet.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// Den importerade stilen har ett utseende som är identiskt med dess källstil.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

Visar hur man klonar ett dokuments stil.

```csharp
Document doc = new Document();

// AddCopy-metoden skapar en kopia av den angivna stilen och
// genererar automatiskt ett nytt namn för stilen, till exempel "Rubrik 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Använd stilens "Namn"-egenskap för att ändra stilens identifierande namn.
newStyle.Name = "My Heading 1";

// Vårt dokument har nu två identiskt utseende stilar med olika namn.
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

* class [Style](../../style/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
