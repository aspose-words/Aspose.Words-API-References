---
title: ListTemplate
second_title: Aspose.Words för .NET API Referens
description: Anger ett av de fördefinierade listformaten som är tillgängliga i Microsoft Word.
type: docs
weight: 3330
url: /sv/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Anger ett av de fördefinierade listformaten som är tillgängliga i Microsoft Word.

```csharp
public enum ListTemplate
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| BulletDefault | `0` | Standard punktlista med 9 nivåer. Kulan på den första nivån är en skiva, kulan på den andra nivån är en cirkel, kulan på den tredje nivån är en kvadrat. Sedan upprepas formateringen för de återstående nivåerna. |
| BulletDisk | `0` | Samma som BulletDefault. |
| BulletCircle | `1` | Kulan på den första nivån är en cirkel. De återstående nivåerna är samma som i BulletDefault. |
| BulletSquare | `2` | Kulan på den första nivån är en kvadrat. De återstående nivåerna är samma som i BulletDefault. |
| BulletDiamonds | `3` | Kulan på den första nivån är en Wingding-karaktär med fyra diamanter. De återstående nivåerna är samma som i BulletDefault. |
| BulletArrowHead | `4` | Kulan på den första nivån är en pilhuvud Wingding-karaktär. De återstående nivåerna är samma som i BulletDefault. |
| BulletTick | `5` | Kulan på den första nivån är en tick Wingding-karaktär. De återstående nivåerna är samma som i BulletDefault. |
| NumberDefault | `6` | Standard numrerad lista med 9 nivåer. Arabisk numrering (1., 2., 3., ...) för den första nivån, numrering av små bokstäver (a., b., c., ...) för den andra nivån, romersk numrering med små bokstäver (i) ., ii., iii., ...) för den tredje nivån. Sedan upprepas formateringen för de återstående nivåerna. |
| NumberArabicDot | `6` | Samma som NumberDefault. |
| NumberArabicParenthesis | `7` | Numret på den första nivån är "1)". De återstående nivåerna är samma som i NumberDefault. |
| NumberUppercaseRomanDot | `8` | Numret på den första nivån är "I." De återstående nivåerna är samma som i NumberDefault. |
| NumberUppercaseLetterDot | `9` | Numret på den första nivån är "A.". De återstående nivåerna är samma som i NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Numret på den första nivån är "a)". De återstående nivåerna är samma som i NumberDefault. |
| NumberLowercaseLetterDot | `11` | Numret på den första nivån är "a.". De återstående nivåerna är samma som i NumberDefault. |
| NumberLowercaseRomanDot | `12` | Numret på den första nivån är "i.". De återstående nivåerna är samma som i NumberDefault. |
| OutlineNumbers | `13` | En översiktslista med nivåerna numrerade "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | En dispositionslista med nivåer är numrerade "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | En disposition listar med olika kulor för olika nivåer. |
| OutlineHeadingsArticleSection | `16` | En dispositionslista med nivåer kopplade till rubrikstilar. |
| OutlineHeadingsLegal | `17` | En dispositionslista med nivåer kopplade till rubrikstilar. |
| OutlineHeadingsNumbers | `18` | En dispositionslista med nivåer kopplade till rubrikstilar. |
| OutlineHeadingsChapter | `19` | En dispositionslista med nivåer kopplade till rubrikstilar. |

### Anmärkningar

Ett listmallvärde används som en parameter i the [`Add`](../listcollection/add) metod.

Aspose.Words listmallar motsvarar de 21 listmallarna available i dialogrutan Bullets and Numbering i Microsoft Word 2003.

### Exempel

Visar hur man skapar ett dokument som innehåller alla listmallar för dispositionsrubriker.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Visar hur man startar om numrering i en lista genom att kopiera en lista.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Tillämpa vår lista på några stycken.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista till dokumentets listsamling
// för att skapa en liknande lista utan att göra ändringar i originalet.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Tillämpa den andra listan på nya stycken.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Visar hur man arbetar med listnivåer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa kapslade listor genom att öka indragsnivån. 
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares "ListFormat"-egenskap. 
// Varje stycke som vi lägger till mellan en listas början och slutet kommer att bli ett objekt i listan.
// Nedan finns två typer av listor som vi kan skapa med hjälp av en dokumentbyggare.
// 1 - En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Genom att ställa in egenskapen "ListLevelNumber" kan vi öka listnivån
// för att starta en fristående underlista vid det aktuella listobjektet.
// Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
// Djupare listnivåer använder bokstäver och gemener romerska siffror. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - En punktlista:
// Denna lista kommer att tillämpa ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i den här listan kommer att använda olika symboler, som "■" och "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Vi kan inaktivera listformatering för att inte formatera några efterföljande stycken som listor genom att avaktivera "List"-flaggan.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Se även

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
