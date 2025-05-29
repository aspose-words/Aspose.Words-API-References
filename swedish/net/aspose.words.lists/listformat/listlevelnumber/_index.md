---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ListFormat ListLevelNumber och hantera enkelt styckelistnivåer från 0 till 8 för förbättrad dokumentorganisation och tydlighet.
type: docs
weight: 40
url: /sv/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Hämtar eller anger listnivånumret (0 till 8) för stycket.

```csharp
public int ListLevelNumber { get; set; }
```

## Anmärkningar

Word-dokument kan listor bestå av 1 eller 9 nivåer, numrerade från 0 till 8.

Har endast effekt när[`List`](../list/) egenskapen är inställd på att referera till en giltig lista.

## Exempel

Visar hur man arbetar med listnivåer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan följer två typer av listor som vi kan skapa med hjälp av en dokumentbyggare.
// 1 - En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje element.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Genom att ställa in egenskapen "ListLevelNumber" kan vi öka listnivån
// för att börja en fristående underlista vid det aktuella listobjektet.
// Listmallen i Microsoft Word som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
 // Djupare listnivåer använder bokstäver och gemener romerska siffror.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - En punktlista:
// Den här listan kommer att lägga till ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i den här listan kommer att använda andra symboler, såsom "■" och "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Vi kan inaktivera listformatering för att inte formatera några efterföljande stycken som listor genom att avaktivera flaggan "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Visar hur man skapar punktlistor och numrerade listor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan följer två typer av listor som vi kan skapa med en dokumentbyggare.
// 1 - En punktlista:
// Den här listan kommer att lägga till ett indrag och en punktsymbol ("•") före varje stycke.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Avsluta punktlistan.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje element.
builder.ListFormat.ApplyNumberDefault();

// Detta stycke är det första objektet. Det första objektet i en numrerad lista kommer att ha en "1." som listobjektsymbol.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Anropa metoden "ListIndent" för att öka den aktuella listnivån,
// vilket startar en ny fristående lista, med ett djupare indrag, vid det aktuella objektet på den första listnivån.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Dessa är de tre första listposterna på den andra listnivån, som kommer att upprätthålla en räkning
// oberoende av antalet för den första listnivån. Enligt det aktuella listformatet,
// de kommer att ha symbolerna "a.", "b." och "c.".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Anropa metoden "ListOutdent" för att återgå till föregående listnivå.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Dessa två stycken fortsätter räkningen för den första listnivån.
// Dessa objekt kommer att ha symbolerna "2." och "3."
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Om vi ökar listnivån till en nivå där vi tidigare har lagt till objekt,
 // den kapslade listan kommer att vara separat från den föregående, och dess numrering börjar från början.
// Dessa listobjekt kommer att ha symbolerna "a.", "b.", "c.", "d." och "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Dra ut listnivån igen.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Avsluta den numrerade listan.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Se även

* class [ListFormat](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
