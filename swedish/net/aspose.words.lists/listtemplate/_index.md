---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Lists.ListTemplate, med fördefinierade listformat i Microsoft Word som enkelt förbättrar presentationen av ditt dokument.
type: docs
weight: 3980
url: /sv/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Anger ett av de fördefinierade listformaten som finns tillgängliga i Microsoft Word.

```csharp
public enum ListTemplate
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| BulletDefault | `0` | Standardpunktlista med 9 nivåer. Punkten för den första nivån är en skiva, punkten för den andra nivån är en cirkel, punkten för den tredje nivån är en kvadrat. Formateringen upprepas sedan för de återstående nivåerna. |
| BulletDisk | `0` | Samma somBulletDefault. |
| BulletCircle | `1` | Punkten på den första nivån är en cirkel. De återstående nivåerna är desamma som iBulletDefault. |
| BulletSquare | `2` | Punkten på den första nivån är en fyrkant. De återstående nivåerna är desamma som iBulletDefault. |
| BulletDiamonds | `3` | Kulan på den första nivån är en Wingding-karaktär med fyra diamanter. De återstående nivåerna är desamma som iBulletDefault. |
| BulletArrowHead | `4` | Punkten på den första nivån är en pilspets Wingding-karaktär. De återstående nivåerna är desamma som iBulletDefault. |
| BulletTick | `5` | Punkten på den första nivån är en tick Wingding-karaktär. De återstående nivåerna är desamma som iBulletDefault. |
| NumberDefault | `6` | Standardnumrerad lista med 9 nivåer. Arabisk numrering (1., 2., 3., ...) för den första nivån, numrering med gemener (a., b., c., ...) för den andra nivån, romersk numrering med gemener (i., ii., iii., ...) för den tredje nivån. Formateringen upprepas sedan för de återstående nivåerna. |
| NumberArabicDot | `6` | Samma somNumberDefault. |
| NumberArabicParenthesis | `7` | Numret på den första nivån är "1)". De återstående nivåerna är samma som iNumberDefault. |
| NumberUppercaseRomanDot | `8` | Numret på den första nivån är "I". De återstående nivåerna är desamma som iNumberDefault. |
| NumberUppercaseLetterDot | `9` | Numret på den första nivån är "A". De återstående nivåerna är desamma som iNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Numret på den första nivån är "a)". De återstående nivåerna är desamma som iNumberDefault. |
| NumberLowercaseLetterDot | `11` | Numret på den första nivån är "a". De återstående nivåerna är desamma som iNumberDefault. |
| NumberLowercaseRomanDot | `12` | Numret på den första nivån är "i". De återstående nivåerna är desamma som iNumberDefault. |
| OutlineNumbers | `13` | En översiktslista med nivåerna numrerade "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | En översiktslista med nivåer är numrerade "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | En översiktlig lista med olika punkter för olika nivåer. |
| OutlineHeadingsArticleSection | `16` | En översiktslista med nivåer kopplade till rubrikformat. |
| OutlineHeadingsLegal | `17` | En översiktslista med nivåer kopplade till rubrikformat. |
| OutlineHeadingsNumbers | `18` | En översiktslista med nivåer kopplade till rubrikformat. |
| OutlineHeadingsChapter | `19` | En översiktslista med nivåer kopplade till rubrikformat. |

## Anmärkningar

Ett listmallvärde används som en parameter i the [`Add`](../listcollection/add/) metod.

Aspose.Words-listmallarna motsvarar de 21 listmallarna som finns tillgängliga i dialogrutan Punkter och numrering i Microsoft Word 2003.

## Exempel

Visar hur man skapar ett dokument som innehåller alla mallar för dispositionsrubriker.

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

Visar hur man startar om numreringen i en lista genom att kopiera en lista.

```csharp
Document doc = new Document();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Tillämpa vår lista på vissa stycken.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista i dokumentets listsamling
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

* namnutrymme [Aspose.Words.Lists](../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../)
