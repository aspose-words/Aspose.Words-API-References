---
title: Class Row
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Tables.Row klass. Representerar en tabellrad.
type: docs
weight: 6310
url: /sv/net/aspose.words.tables/row/
---
## Row class

Representerar en tabellrad.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public class Row : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Row](row/)(DocumentBase) | Initierar en ny instans av`Row` class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | Ger maskinskriven åtkomst till[`Cell`](../cell/) underordnade noder för raden. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | Returnerar den första[`Cell`](../cell/) i raden. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | True om detta är den första raden i en tabell; falskt annars. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | Sant om detta är den sista raden i en tabell; falskt annars. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | Returnerar den sista[`Cell`](../cell/) i raden. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [NextRow](../../aspose.words.tables/row/nextrow/) { get; } | Får nästa`Row` nod. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | ReturnerarRow . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | Returnerar den omedelbara överordnade tabellen för raden. |
| [PreviousRow](../../aspose.words.tables/row/previousrow/) { get; } | Hämtar föregående`Row` nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | Ger tillgång till formateringsegenskaperna för raden. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(DocumentVisitor) | Accepterar en besökare. |
| override [AcceptEnd](../../aspose.words.tables/row/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.tables/row/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | Om`Row` har inga celler, skapar och lägger till en[`Cell`](../cell/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | Hämtar texten för alla celler i den här raden inklusive slutet av radens tecken. |
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
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

`Row` kan bara vara ett barn till en[`Table`](../table/).

`Row` kan innehålla en eller flera[`Cell`](../cell/) knutpunkter.

En minsta giltig rad måste ha minst en[`Cell`](../cell/).

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


