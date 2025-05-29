---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Tables.Table för att enkelt skapa och hantera tabeller i Word-dokument, vilket förbättrar dokumentets layout och funktionalitet.
type: docs
weight: 7190
url: /sv/net/aspose.words.tables/table/
---
## Table class

Representerar en tabell i ett Word-dokument.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public class Table : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initierar en ny instans av`Table` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Hämtar eller ställer in absolut horisontell flytande tabellposition som anges av tabellegenskaperna, i punkter. Standardvärdet är 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Hämtar eller ställer in den absoluta vertikala flytande tabellpositionen som anges av tabellegenskaperna, i punkter. Standardvärdet är 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Anger hur en inbäddad tabell är justerad i dokumentet. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar deras innehåll. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Hämtar eller ställer in alternativet "Tillåt avstånd mellan celler". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Hämtar om en flytande tabell ska tillåta andra flytande objekt i dokumentet att överlappa dess omfattning när den visas. Standardvärdet är`sann` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Hämtar eller anger om detta är en tabell som skrivs från höger till vänster. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under innehållet i cellerna. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) mellan cellerna. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Hämtar eller anger beskrivning av denna tabell. Den ger en alternativ textrepresentation av informationen i tabellen. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellens botten och den omgivande texten, i punkter. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellens vänstra sida och den omgivande texten, i punkter. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellens högra sida och den omgivande texten, i punkter. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Hämtar eller ställer in avståndet mellan bordsskivan och den omgivande texten, i punkter. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Returnerar det första[`Row`](../row/) nod i tabellen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Hämtar basobjektet från vilket den horisontella positioneringen av den flytande tabellen ska beräknas. Standardvärdet ärColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Returnerar det sista[`Row`](../row/) nod i tabellen. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Hämtar eller anger värdet som representerar tabellens vänstra indrag. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till vänster om innehållet i cellerna. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | ReturerTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Hämtar eller ställer in tabellens önskade bredd. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Hämtar eller ställer in den flytande tabellens relativa horisontella justering. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Hämtar eller ställer in den flytande tabellens relativa vertikala justering. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till till höger om innehållet i cellerna. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Ger åtkomst till tabellens rader med maskinskriven kod. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Hämtar eller ställer in tabellstilen som tillämpas på den här tabellen. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Hämtar eller ställer in den språkoberoende stilidentifieraren för tabellstilen som tillämpats på den här tabellen. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Hämtar eller anger namnet på tabellformatet som tillämpats på den här tabellen. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Hämtar eller ställer in bitflaggor som anger hur en tabellstil tillämpas på den här tabellen. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Hämtar eller sätter[`TextWrapping`](./textwrapping/) för tabell. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Hämtar eller anger titeln för denna tabell. Tillhandahåller en alternativ textrepresentation av informationen i tabellen. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Hämtar eller anger mängden utrymme (i punkter) som ska läggas till ovanför innehållet i cellerna. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Hämtar basobjektet från vilket den vertikala positioneringen av den flytande tabellen ska beräknas. Standardvärdet ärMargin . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av bordet. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av bordet. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Ändrar storleken på tabellen och cellerna enligt det angivna automatiska anpassningsbeteendet. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Tar bort alla tabell- och cellkanter i den här tabellen. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Tar bort all skuggning på tabellen. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Konverterar celler som sammanfogats horisontellt efter bredd till celler som sammanfogats efter[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Om tabellen inte har några rader, skapas och läggs till en[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Ställer in den angivna tabellkanten till den angivna linjestilen, bredden och färgen. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Ställer in alla tabellkanter till angiven linjestil, bredd och färg. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Ställer in skuggning till de angivna värdena för hela tabellen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

`Table` är en blocknivånod och kan vara ett barn till klasser som härrör från[`Story`](../../aspose.words/story/) eller [`InlineStory`](../../aspose.words/inlinestory/).

`Table` kan innehålla en eller flera[`Row`](../row/) noder.

En minimal giltig tabell måste ha minst en[`Row`](../row/).

## Exempel

Visar hur man skapar en tabell.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabeller innehåller rader, som innehåller celler, vilka kan innehålla stycken
// med typiska element som körningar, former och även andra tabeller.
// Att anropa metoden "EnsureMinimum" på en tabell säkerställer att
// tabellen har minst en rad, cell och stycke.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Lägg till text i den första cellen på den första raden i tabellen.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Visar hur man itererar igenom alla tabeller i dokumentet och skriver ut innehållet i varje cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Vi kan använda metoden "ToArray" på en radsamling för att klona den till en array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Vi kan använda metoden "ToArray" på en cellsamling för att klona den till en array.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Visar hur man bygger en formaterad 2x2-tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// När tabellen skapas kommer dokumentbyggaren att tillämpa dess aktuella RowFormat/CellFormat-egenskapsvärden
// till den aktuella raden/cellen där markören befinner sig och alla nya rader/celler allt eftersom de skapas.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Tidigare tillagda rader och celler påverkas inte retroaktivt av ändringar i formateringen i verktyget.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Visar hur man bygger en kapslad tabell utan att använda en dokumentbyggare.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Skapa den yttre tabellen med tre rader och fyra kolumner och lägg sedan till den i dokumentet.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Skapa en annan tabell med två rader och två kolumner och infoga den sedan i den första tabellens första cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Skapar en ny tabell i dokumentet med de angivna dimensionerna och texten i varje cell.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Du kan använda egenskaperna "Titel" och "Beskrivning" för att lägga till en titel respektive beskrivning till din tabell.
    // Tabellen måste ha minst en rad innan vi kan använda dessa egenskaper.
    // Dessa egenskaper är betydelsefulla för ISO/IEC 29500-kompatibla .docx-dokument (se OoxmlCompliance-klassen).
    // Om vi sparar dokumentet i format före ISO/IEC 29500 ignorerar Microsoft Word dessa egenskaper.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode/)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
