---
title: DocumentBase.Lists
linktitle: Lists
articleTitle: Lists
second_title: Aspose.Words för .NET
description: Upptäck DocumentBase-listor för effektiv fastighetshantering. Få tillgång till anpassningsbar listformatering för att förbättra dokumentets presentation och tydlighet.
type: docs
weight: 50
url: /sv/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

Ger åtkomst till listformateringen som används i dokumentet.

```csharp
public ListCollection Lists { get; }
```

## Anmärkningar

För mer information se beskrivningen av[`ListCollection`](../../../aspose.words.lists/listcollection/) klass.

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

### Se även

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
