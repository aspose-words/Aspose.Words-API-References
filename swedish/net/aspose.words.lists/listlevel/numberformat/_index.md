---
title: NumberFormat
second_title: Aspose.Words för .NET API Referens
description: Returnerar eller ställer in talformatet för listnivån.
type: docs
weight: 70
url: /sv/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Returnerar eller ställer in talformatet för listnivån.

```csharp
public string NumberFormat { get; set; }
```

### Anmärkningar

Bland vanliga texttecken kan strängen innehålla platshållartecken \x0000 till \x0008 som representerar siffrorna från motsvarande listnivåer.

Till exempel kommer strängen "\x0000.\x0001)" att generera en lista label som ser ut ungefär som "1.5)". Siffran "1" är det aktuella numret från den 1:a listnivån, siffran "5" är det aktuella numret från den 2:a listnivån.

Null är inte tillåtet, men en tom sträng betyder att inget nummer är giltigt.

### Exempel

Visar hur du använder anpassad listformatering på stycken när du använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första av listnivåerna.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Detta NumberFormat-värde skapar stjärnformade punktlistsymboler.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Skapa stycken och tillämpa båda listnivåerna i vår anpassade listformatering på dem.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

Visar avancerade sätt att anpassa listetiketter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Nivå 1-etiketter kommer att formateras enligt styckeformatet "Rubrik 1" och kommer att ha ett prefix.
// Dessa kommer att se ut som "Bilaga A", "Bilaga B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Nivå 2-etiketter visar de aktuella numren på den första och andra listnivån och har inledande nollor.
// Om den första listnivån är på 1, kommer listetiketterna från dessa att se ut som "Avsnitt (1.01)", "Sektion (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Observera att den högre nivån använder numrering av versaler.
// Vi kan ställa in egenskapen "IsLegal" för att använda arabiska siffror för de högre listnivåerna.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Nivå 3-etiketter kommer att vara romerska siffror med stora bokstäver med ett prefix och ett suffix och kommer att starta om vid varje Listnivå 1-objekt.
// Dessa listetiketter kommer att se ut som "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Gör etiketter för alla listnivåer i fetstil.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Använd listformatering på det aktuella stycket.
builder.ListFormat.List = list;

// Skapa listobjekt som visar alla våra tre listnivåer.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Se även

* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../listlevel/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
