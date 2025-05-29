---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Tables.Table per creare e gestire facilmente le tabelle nei documenti Word, migliorando il layout e la funzionalità del documento.
type: docs
weight: 7190
url: /it/net/aspose.words.tables/table/
---
## Table class

Rappresenta una tabella in un documento Word.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public class Table : CompositeNode
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Inizializza una nuova istanza di`Table` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Ottiene o imposta la posizione assoluta orizzontale della tabella mobile specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Ottiene o imposta la posizione assoluta della tabella mobile verticale specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Specifica come una tabella in linea viene allineata nel documento. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle di una tabella per adattarle al loro contenuto. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Ottiene o imposta l'opzione "Consenti spaziatura tra le celle". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Ottiene se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando vengono visualizzati. Il valore predefinito è `VERO` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Ottiene o imposta se questa è una tabella da destra a sinistra. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) tra le celle. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Ottiene o imposta la descrizione di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Ottiene o imposta la distanza tra il fondo della tabella e il testo circostante, in punti. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Ottiene o imposta la distanza tra la parte sinistra della tabella e il testo circostante, in punti. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Ottiene o imposta la distanza tra la parte destra della tabella e il testo circostante, in punti. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Ottiene o imposta la distanza tra il piano del tavolo e il testo circostante, in punti. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Restituisce il primo[`Row`](../row/) nodo nella tabella. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Ottiene l'oggetto base da cui deve essere calcolato il posizionamento orizzontale della tabella mobile. Il valore predefinito èColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Restituisce l'ultimo[`Row`](../row/) nodo nella tabella. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Ottiene o imposta il valore che rappresenta il rientro sinistro della tabella. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | RestituisceTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Ottiene o imposta la larghezza preferita della tabella. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Ottiene o imposta l'allineamento orizzontale relativo della tabella mobile. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Ottiene o imposta l'allineamento verticale relativo della tabella mobile. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Fornisce accesso tipizzato alle righe della tabella. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Ottiene o imposta lo stile tabella applicato a questa tabella. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni locali dello stile di tabella applicato a questa tabella. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Ottiene o imposta il nome dello stile tabella applicato a questa tabella. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Ottiene o imposta i flag di bit che specificano come uno stile di tabella viene applicato a questa tabella. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Ottiene o imposta[`TextWrapping`](./textwrapping/) per la tabella. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Ottiene o imposta il titolo di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Ottiene l'oggetto base da cui deve essere calcolato il posizionamento verticale della tabella mobile. Il valore predefinito èMargin . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore che raggiunge la fine della tabella. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio della tabella. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Rimuove tutti i bordi delle tabelle e delle celle in questa tabella. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Rimuove tutte le ombreggiature sulla tabella. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Converte le celle unite orizzontalmente per larghezza in celle unite per[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Se la tabella non ha righe, ne crea e ne aggiunge una[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Imposta il bordo della tabella specificato sullo stile di linea, sulla larghezza e sul colore specificati. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Imposta tutti i bordi della tabella sullo stile di linea, la larghezza e il colore specificati. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Imposta l'ombreggiatura sui valori specificati sull'intera tabella. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

`Table` è un nodo a livello di blocco e può essere un figlio di classi derivate da[`Story`](../../aspose.words/story/) oppure [`InlineStory`](../../aspose.words/inlinestory/).

`Table` può contenere uno o più[`Row`](../row/) nodi.

Una tabella minima valida deve avere almeno uno[`Row`](../row/).

## Esempi

Mostra come creare una tabella.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Le tabelle contengono righe, che contengono celle, che possono avere paragrafi
// con elementi tipici quali sequenze, forme e persino altre tabelle.
// La chiamata al metodo "EnsureMinimum" su una tabella garantirà che
// la tabella ha almeno una riga, una cella e un paragrafo.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Aggiunge testo alla prima cella della prima riga della tabella.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Mostra come scorrere tutte le tabelle del documento e stampare il contenuto di ogni cella.

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

Mostra come creare una tabella formattata 2x2.

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

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti delle proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che vengono create.
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

// Le righe e le celle aggiunte in precedenza non vengono retroattivamente influenzate dalle modifiche apportate alla formattazione del builder.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Mostra come creare una tabella nidificata senza utilizzare un generatore di documenti.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Crea la tabella esterna con tre righe e quattro colonne, quindi aggiungila al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crea un'altra tabella con due righe e due colonne e inseriscila nella prima cella della prima tabella.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nuova tabella nel documento con le dimensioni specificate e il testo in ogni cella.
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
    // Queste proprietà sono significative per i documenti .docx conformi allo standard ISO/IEC 29500 (vedere la classe OoxmlCompliance).
    // Se salviamo il documento in formati precedenti a ISO/IEC 29500, Microsoft Word ignora queste proprietà.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Guarda anche

* class [CompositeNode](../../aspose.words/compositenode/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
