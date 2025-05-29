---
title: Row Class
linktitle: Row
articleTitle: Row
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Tables.Row för sömlös hantering av tabellrader i dina dokument. Förbättra din dokumenthantering med kraftfulla funktioner!
type: docs
weight: 7160
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
| [Row](row/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initierar en ny instans av`Row` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | Ger maskinskriven åtkomst till[`Cell`](../cell/) underordnade noder till raden. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | Returnerar det första[`Cell`](../cell/) i raden. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | Sant om detta är den första raden i en tabell; annars falskt. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | Sant om detta är den sista raden i en tabell; annars falskt. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | Returnerar det sista[`Cell`](../cell/) i raden. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [NextRow](../../aspose.words.tables/row/nextrow/) { get; } | Får nästa`Row` nod. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | ReturerRow . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | Returnerar den omedelbara överordnade tabellen för raden. |
| [PreviousRow](../../aspose.words.tables/row/previousrow/) { get; } | Hämtar föregående`Row` nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | Ger åtkomst till formateringsegenskaperna för raden. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.tables/row/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av raden. |
| override [AcceptStart](../../aspose.words.tables/row/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av raden. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | Om`Row` har inga celler, skapar och lägger till en[`Cell`](../cell/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | Hämtar texten för alla celler i den här raden inklusive radslutstecknet. |
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
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

`Row` kan bara vara ett barn till en[`Table`](../table/).

`Row` kan innehålla en eller flera[`Cell`](../cell/) noder.

En giltig rad måste ha minst en[`Cell`](../cell/).

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
