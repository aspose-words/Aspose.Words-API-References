---
title: ListLevel.IsLegal
second_title: Aspose.Words för .NET API Referens
description: ListLevel fast egendom. Sant om nivån ändrar alla ärvda tal till arabiska falskt om den bevarar deras talstil.
type: docs
weight: 50
url: /sv/net/aspose.words.lists/listlevel/islegal/
---
## ListLevel.IsLegal property

Sant om nivån ändrar alla ärvda tal till arabiska, falskt om den bevarar deras talstil.

```csharp
public bool IsLegal { get; set; }
```

### Exempel

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


