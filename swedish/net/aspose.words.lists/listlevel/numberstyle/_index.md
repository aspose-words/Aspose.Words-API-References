---
title: ListLevel.NumberStyle
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListLevel NumberStyle för att enkelt anpassa och ställa in numeriska stilar för dina listor, vilket förbättrar organisationen och tydligheten.
type: docs
weight: 90
url: /sv/net/aspose.words.lists/listlevel/numberstyle/
---
## ListLevel.NumberStyle property

Returnerar eller anger numerisk stil för denna listnivå.

```csharp
public NumberStyle NumberStyle { get; set; }
```

## Exempel

Visar hur man använder anpassad listformatering på stycken när man använder DocumentBuilder.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa de två första listnivåerna.
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
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Nivå 1-etiketter formateras enligt styckeformatet "Rubrik 1" och har ett prefix.
// Dessa kommer att se ut som "Bilaga A", "Bilaga B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Etiketter för nivå 2 visar de aktuella numren för den första och andra listnivån och har inledande nollor.
// Om den första listnivån är på 1, kommer listetiketterna från dessa att se ut som "Avsnitt (1.01)", "Avsnitt (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Observera att den högre nivån använder numrering med versaler.
// Vi kan ställa in egenskapen "IsLegal" så att den använder arabiska siffror för de högre listnivåerna.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Nivå 3-etiketter kommer att vara romerska siffror i versaler med ett prefix och ett suffix och börjar om vid varje objekt på listnivå 1.
// Dessa listetiketter kommer att se ut som "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Gör etiketter för alla listnivåer fetstilta.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Tillämpa listformatering på det aktuella stycket.
builder.ListFormat.List = list;

// Skapa listobjekt som visar alla tre listnivåer.
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

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
