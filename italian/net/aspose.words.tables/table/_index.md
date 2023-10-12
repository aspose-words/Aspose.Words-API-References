---
title: Class Table
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.Table classe. Rappresenta una tabella in un documento Word.
type: docs
weight: 6340
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
| [Table](table/)(DocumentBase) | Inizializza una nuova istanza di`Table` classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Ottiene o imposta la posizione assoluta della tabella mobile orizzontale specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Ottiene o imposta la posizione assoluta della tabella mobile verticale specificata dalle proprietà della tabella, in punti. Il valore predefinito è 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Specifica come viene allineata una tabella in linea nel documento. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle in una tabella per adattarle al contenuto. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Ottiene o imposta l'opzione "Consenti spaziatura tra celle". |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Indica se una tabella mobile deve consentire ad altri oggetti mobili nel documento di sovrapporsi alle sue estensioni quando viene visualizzato. Il valore predefinito è`VERO` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Ottiene o imposta se si tratta di una tabella da destra a sinistra. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) tra le celle. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Ottiene o imposta la descrizione di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Ottiene o imposta la distanza tra il fondo della tabella e il testo circostante, in punti. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Ottiene o imposta la distanza tra la tabella a sinistra e il testo circostante, in punti. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Ottiene o imposta la distanza in punti tra la destra della tabella e il testo circostante. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Ottiene o imposta la distanza tra il piano del tavolo e il testo circostante, in punti. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Restituisce il primo[`Row`](../row/) nodo nella tabella. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figli. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Ottiene l'oggetto base da cui calcolare il posizionamento orizzontale della tabella mobile. Il valore predefinito èColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figli. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Restituisce l'ultimo[`Row`](../row/) nodo nella tabella. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Ottiene o imposta il valore che rappresenta il rientro sinistro della tabella. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | RestituisceTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Ottiene o imposta la larghezza preferita della tabella. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce a[`Range`](../../aspose.words/range/) oggetto che rappresenta la porzione di documento contenuta in questo nodo. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Ottiene o imposta l'allineamento orizzontale relativo della tabella mobile. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Ottiene o imposta l'allineamento verticale relativo della tabella mobile. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Fornisce l'accesso digitato alle righe della tabella. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Ottiene o imposta lo stile di tabella applicato a questa tabella. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni locali dello stile di tabella applicato a questa tabella. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Ottiene o imposta il nome dello stile di tabella applicato a questa tabella. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Ottiene o imposta flag di bit che specificano come viene applicato uno stile di tabella a questa tabella. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Ottiene o imposta[`TextWrapping`](./textwrapping/) per tavolo. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Ottiene o imposta il titolo di questa tabella. Fornisce una rappresentazione testuale alternativa delle informazioni contenute nella tabella. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Ottiene l'oggetto base da cui deve essere calcolato il posizionamento verticale della tabella mobile. Il valore predefinito èMargin . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(DocumentVisitor) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](../../aspose.words.tables/table/autofit/)(AutoFitBehavior) | Ridimensiona la tabella e le celle in base al comportamento di adattamento automatico specificato. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Rimuove tutti i bordi della tabella e delle celle su questa tabella. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Rimuove tutte le ombre sul tavolo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Converte le celle unite orizzontalmente per larghezza in celle unite per[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Se la tabella non ha righe, ne crea e ne aggiunge una[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Restituisce una raccolta attiva di nodi secondari che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce il supporto per l'iterazione di ogni stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Restituisce l'indice del nodo figlio specificato nell'array di nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/)nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(BorderType, LineStyle, double, Color, bool) | Imposta il bordo della tabella specificato sullo stile di linea, larghezza e colore specificati. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(LineStyle, double, Color) | Imposta tutti i bordi della tabella sullo stile di linea, larghezza e colore specificati. |
| [SetShading](../../aspose.words.tables/table/setshading/)(TextureIndex, Color, Color) | Imposta l'ombreggiatura sui valori specificati sull'intera tabella. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

### Osservazioni

`Table`è un nodo a livello di blocco e può essere figlio di classi derivate da[`Story`](../../aspose.words/story/) oppure [`InlineStory`](../../aspose.words/inlinestory/).

`Table` può contenerne uno o più[`Row`](../row/) nodi.

Una tabella minima valida deve averne almeno una[`Row`](../row/).

### Esempi

Mostra come creare una tabella.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Le tabelle contengono righe, che contengono celle, che possono avere paragrafi
// con elementi tipici come percorsi, forme e persino altre tabelle.
// La chiamata al metodo "EnsureMinimum" su una tabella lo garantirà
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

Mostra come scorrere tutte le tabelle del documento e stampare il contenuto di ciascuna cella.

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

        // Possiamo utilizzare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
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

Mostra come creare una tabella 2x2 formattata.

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

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti della proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a qualsiasi nuova riga/cella mentre le crea.
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

// Le righe e le celle aggiunte in precedenza non vengono influenzate retroattivamente dalle modifiche alla formattazione del builder.
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

    // Crea un'altra tabella con due righe e due colonne e quindi inseriscila nella prima cella della prima tabella.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nuova tabella nel documento con le dimensioni e il testo specificati in ogni cella.
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


