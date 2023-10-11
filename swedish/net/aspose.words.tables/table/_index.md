---
title: Class Table
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Tables.Table klass. Representerar en tabell i ett Worddokument.
type: docs
weight: 6340
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
| [Table](table/)(DocumentBase) | Initierar en ny instans av`Table` class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Hämtar eller ställer in absolut horisontell flytande tabellposition specificerad av tabellegenskaperna, i poäng. Standardvärdet är 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Hämtar eller ställer in den absoluta vertikala flytande tabellens position specificerad av tabellens egenskaper, i poäng. Standardvärdet är 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Anger hur en inlinetabell justeras i dokumentet. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Tillåter Microsoft Word och Aspose.Words att automatiskt ändra storlek på celler i en tabell så att de passar deras innehåll. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Hämtar eller ställer in alternativet "Tillåt avstånd mellan celler". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Hämtar om en flytande tabell ska tillåta andra flytande objekt i document att överlappa dess omfattning när den visas. Standardvärdet är`Sann` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Hämtar eller ställer in om detta är en tabell från höger till vänster. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till under innehållet i celler. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) mellan cellerna. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Hämtar eller ställer in en beskrivning av denna tabell. Den ger en alternativ textrepresentation av informationen i tabellen. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellbotten och den omgivande texten, i punkter. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellen till vänster och den omgivande texten, i punkter. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Hämtar eller ställer in avståndet mellan tabellens högra sida och den omgivande texten, i punkter. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Hämtar eller ställer in avståndet mellan bordsskivan och den omgivande texten, i punkter. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Returnerar den första[`Row`](../row/) nod i tabellen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Hämtar basobjektet från vilket den horisontella positioneringen av flytande tabell ska beräknas. Standardvärdet ärColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Returnerar den sista[`Row`](../row/) nod i tabellen. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Hämtar eller ställer in värdet som representerar den vänstra indraget i tabellen. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till vänster om innehållet i celler. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | ReturnerarTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Hämtar eller ställer in tabellens föredragna bredd. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Hämtar eller ställer in flytande tabell relativ horisontell justering. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Hämtar eller ställer in flytande tabell relativ vertikal justering. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till höger om innehållet i celler. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Ger maskinskriven åtkomst till raderna i tabellen. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Hämtar eller ställer in tabellstilen som tillämpas på denna tabell. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Hämtar eller ställer in den språkoberoende stilidentifieraren för tabellstilen som tillämpas på denna tabell. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Hämtar eller ställer in namnet på tabellformatet som tillämpas på denna tabell. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Hämtar eller ställer in bitflaggor som anger hur en tabellstil tillämpas på den här tabellen. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Hämtar eller sätter[`TextWrapping`](./textwrapping/) för tabell. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Hämtar eller ställer in titeln på denna tabell. Den ger en alternativ textrepresentation av informationen i tabellen. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till ovanför innehållet i celler. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Hämtar basobjektet från vilket den vertikala positioneringen av flytande tabell ska beräknas. Standardvärdet ärMargin . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(DocumentVisitor) | Accepterar en besökare. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](../../aspose.words.tables/table/autofit/)(AutoFitBehavior) | Ändrar storlek på tabellen och cellerna enligt det angivna beteendet för automatisk anpassning. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Tar bort alla tabell- och cellkanter på den här tabellen. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Tar bort all skuggning på bordet. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Konverterar celler horisontellt sammanfogade efter bredd till celler sammanslagna av[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Om tabellen inte har några rader, skapar och lägger till en[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(BorderType, LineStyle, double, Color, bool) | Ställer in den angivna tabellkanten till angiven linjestil, bredd och färg. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(LineStyle, double, Color) | Ställer in alla tabellkanter till angiven linjestil, bredd och färg. |
| [SetShading](../../aspose.words.tables/table/setshading/)(TextureIndex, Color, Color) | Ställer in skuggning till de angivna värdena på hela tabellen. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

`Table`är en nod på blocknivå och kan vara ett barn av klasser som härrör från[`Story`](../../aspose.words/story/) or [`InlineStory`](../../aspose.words/inlinestory/).

`Table` kan innehålla en eller flera[`Row`](../row/) knutpunkter.

En minsta giltig tabell måste ha minst en[`Row`](../row/).

### Exempel

Visar hur man skapar en tabell.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabeller innehåller rader, som innehåller celler, som kan ha stycken
// med typiska element som körningar, former och till och med andra tabeller.
// Att anropa metoden "EnsureMinimum" på en tabell säkerställer det
// tabellen har minst en rad, cell och stycke.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Lägg till text till det första anropet i den första raden i tabellen.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Visar hur man itererar genom alla tabeller i dokumentet och skriver ut innehållet i varje cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Vi kan använda "ToArray"-metoden på en radsamling för att klona den till en array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Vi kan använda "ToArray"-metoden på en cellsamling för att klona den till en array.
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

// När du bygger tabellen kommer dokumentbyggaren att tillämpa sina nuvarande RowFormat/CellFormat-egenskapsvärden
// till den aktuella raden/cellen som markören är i och eventuella nya rader/celler när den skapar dem.
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

// Tidigare tillagda rader och celler påverkas inte retroaktivt av ändringar i byggarens formatering.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Visar hur man bygger en kapslad tabell utan att använda ett dokumentbyggare.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Skapa den yttre tabellen med tre rader och fyra kolumner och lägg sedan till den i dokumentet.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Skapa ytterligare en tabell med två rader och två kolumner och infoga den sedan i den första tabellens första cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Skapar en ny tabell i dokumentet med givna dimensioner och text i varje cell.
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

    // Du kan använda egenskaperna "Titel" och "Beskrivning" för att lägga till en titel respektive en beskrivning till din tabell.
    // Tabellen måste ha minst en rad innan vi kan använda dessa egenskaper.
    // Dessa egenskaper är meningsfulla för ISO / IEC 29500-kompatibla .docx-dokument (se klassen OoxmlCompliance).
    // Om vi sparar dokumentet i pre-ISO/IEC 29500-format ignorerar Microsoft Word dessa egenskaper.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode/)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)


