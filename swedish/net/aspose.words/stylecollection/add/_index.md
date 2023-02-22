---
title: StyleCollection.Add
second_title: Aspose.Words för .NET API Referens
description: StyleCollection metod. Skapar en ny användardefinierad stil och lägger till den i samlingen.
type: docs
weight: 60
url: /sv/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Skapar en ny användardefinierad stil och lägger till den i samlingen.

```csharp
public Style Add(StyleType type, string name)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| type | StyleType | A[`StyleType`](../../styletype/) värde som anger vilken typ av stil som ska skapas. |
| name | String | Skiftlägeskänsligt namn på stilen som ska skapas. |

### Anmärkningar

Du kan skapa tecken, stycke eller en liststil.

När du skapar en liststil skapas stilen med standard numrerad listformatering (1 \ a \ i).

Kastar ett undantag om en stil med detta namn redan finns.

### Exempel

Visar hur man lägger till en stil till ett dokuments stilsamling.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";

// Om vi lägger till en stil av "StyleType.Paragraph", kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

Visar hur du skapar en liststil och använder den i ett dokument.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Vi kan innehålla ett helt List-objekt i en stil.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändra utseendet på alla listnivåer i vår lista.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Skapa en annan lista från en lista inom en stil.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Lägg till några listobjekt som vår lista kommer att formatera.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Skapa och tillämpa en annan lista baserat på liststilen.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Se även

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../stylecollection/)
* hopsättning [Aspose.Words](../../../)


