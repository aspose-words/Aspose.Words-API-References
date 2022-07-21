---
title: Cell
second_title: Aspose.Words för .NET API Referens
description: Representerar en tabellcell.
type: docs
weight: 5940
url: /sv/net/aspose.words.tables/cell/
---
## Cell class

Representerar en tabellcell.

```csharp
public class Cell : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Cell](cell)(DocumentBase) | Initierar en ny instans av **Cell** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | Ger tillgång till cellens formateringsegenskaper. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [Count](../../aspose.words/compositenode/count) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | Får första stycket bland de närmaste barnen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | Sant om detta är den första cellen i en rad; falskt annars. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | Sant om detta är den sista cellen i en rad; falskt annars. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | Får det sista stycket bland de närmaste barnen. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | Returnerar **NodeType.Cell** . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | Får en samling stycken som är omedelbara barn till cellen. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | Returnerar cellens överordnade rad. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | Hämtar en samling tabeller som är omedelbart underordnade cellen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserverad för systemanvändning. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | Om det sista underordnade inte är ett stycke, skapar och lägger till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag) underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

**Cell** kan bara vara ett barn till en **Rad**.

**Cell** kan innehålla noder på blocknivå **Paragraf** och **Tabell**.

En minimal giltig cell måste ha minst en **Paragraf**.

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

* class [CompositeNode](../../aspose.words/compositenode)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
