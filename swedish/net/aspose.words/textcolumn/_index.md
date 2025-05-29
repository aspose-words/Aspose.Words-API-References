---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.TextColumn för att hantera textkolumner i dina dokument. Få enkelt åtkomst till och anpassa varje kolumn i ditt textavsnitt.
type: docs
weight: 7240
url: /sv/net/aspose.words/textcolumn/
---
## TextColumn class

Representerar en enda textkolumn.`TextColumn` är medlem i[`TextColumnCollection`](../textcolumncollection/) samling. Den`TextColumn`samlingen innehåller alla kolumner i ett avsnitt av ett dokument.

För att lära dig mer, besök[Arbeta med sektioner](https://docs.aspose.com/words/net/working-with-sections/) dokumentationsartikel.

```csharp
public class TextColumn
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Hämtar eller ställer in avståndet mellan denna kolumn och nästa kolumn i punkter. Krävs inte för den sista kolumnen. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Hämtar eller ställer in bredden på textkolumnen i punkter. |

## Anmärkningar

`TextColumn` objekt används bara för att ange kolumner med anpassad bredd och avstånd. Om du vill att kolumnerna i dokumentet ska ha samma bredd, ange TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) till`sann`.

När en ny`TextColumn` skapas har den sin bredd och sitt avstånd satt till noll.

## Exempel

Visar hur man skapar ojämnt fördelade kolumner.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Bestäm hur mycket utrymme vi har tillgängligt för att arrangera kolumner.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Sätt den första kolumnen till att vara smal.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Ställ in den andra kolumnen så att den tar upp resten av det tillgängliga utrymmet inom sidans marginaler.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
