---
title: DocumentBuilder.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words för .NET
description: Utforska egenskapen ListFormat i DocumentBuilder för att komma åt och anpassa dina nuvarande listformateringsinställningar för förbättrad dokumentdesign.
type: docs
weight: 150
url: /sv/net/aspose.words/documentbuilder/listformat/
---
## DocumentBuilder.ListFormat property

Returnerar ett objekt som representerar aktuella listformateringsegenskaper.

```csharp
public ListFormat ListFormat { get; }
```

## Exempel

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
