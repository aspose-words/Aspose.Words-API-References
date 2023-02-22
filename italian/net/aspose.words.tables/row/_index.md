---
title: Class Row
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.Row classe. Rappresenta una riga di tabella.
type: docs
weight: 6010
url: /it/net/aspose.words.tables/row/
---
## Row class

Rappresenta una riga di tabella.

```csharp
public class Row : CompositeNode
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Row](row/)(DocumentBase) | Inizializza una nuova istanza di **Riga** classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | Fornisce l'accesso tipizzato al file **Cellula** nodi figlio della riga. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ottiene tutti i nodi figlio immediati di questo nodo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | Restituisce il primo **Cellula** nella riga. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce true se questo nodo ha nodi figlio. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce true poiché questo nodo può avere nodi figlio. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | True se questa è la prima riga in una tabella; falso altrimenti. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | True se questa è l'ultima riga in una tabella; falso altrimenti. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | Restituisce l'ultimo **Cellula** nella riga. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | Restituisce **TipoNodo.Riga** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | Restituisce la tabella padre immediato della riga. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | Fornisce l'accesso alle proprietà di formattazione della riga. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(DocumentVisitor) | Accetta un visitatore. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Riservato per l'uso del sistema. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | Se il **Riga** non ha celle, ne crea e ne aggiunge una **Cellula** . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Restituisce un ennesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | Ottiene il testo di tutte le celle in questa riga, incluso il carattere di fine riga. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Restituisce l'indice del nodo figlio specificato nell'array del nodo figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo nodo che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

**Riga** può essere solo figlio di a **Tavolo**.

**Riga** può contenerne uno o più **Cellula** nodi.

Una riga valida minima deve averne almeno una **Cellula**.

### Esempi

Mostra come creare una tabella.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Le tabelle contengono righe, che contengono celle, che possono avere paragrafi
// con elementi tipici come piste, forme e persino altre tabelle.
// Chiamare il metodo "EnsureMinimum" su una tabella lo garantirà
// la tabella ha almeno una riga, una cella e un paragrafo.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Aggiunge testo alla prima chiamata nella prima riga della tabella.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Mostra come scorrere tutte le tabelle nel documento e stampare il contenuto di ogni cella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Possiamo usare il metodo "ToArray" su una raccolta di righe per clonarla in un array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Possiamo usare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
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

Mostra come creare una tabella nidificata senza utilizzare un generatore di documenti.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Crea la tabella esterna con tre righe e quattro colonne, quindi aggiungila al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crea un'altra tabella con due righe e due colonne, quindi inseriscila nella prima cella della prima tabella.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nuova tabella nel documento con le dimensioni e il testo indicati in ogni cella.
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

    // Puoi utilizzare le proprietà "Titolo" e "Descrizione" per aggiungere rispettivamente un titolo e una descrizione alla tua tabella.
    // La tabella deve avere almeno una riga prima di poter utilizzare queste proprietà.
    // Queste proprietà sono significative per i documenti .docx conformi a ISO / IEC 29500 (vedere la classe OoxmlCompliance).
    // Se salviamo il documento in formati pre-ISO/IEC 29500, Microsoft Word ignora queste proprietà.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Guarda anche

* class [CompositeNode](../../aspose.words/compositenode/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)


