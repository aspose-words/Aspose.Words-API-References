---
title: Class ConditionalStyleCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ConditionalStyleCollection classe. Rappresenta una raccolta diConditionalStyle oggetti.
type: docs
weight: 310
url: /it/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Rappresenta una raccolta di[`ConditionalStyle`](../conditionalstyle/) oggetti.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Ottiene lo stile della cella in basso a sinistra. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Ottiene lo stile della cella in basso a destra. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Ottiene il numero di stili condizionali nella raccolta. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Ottiene lo stile di raggruppamento delle colonne pari. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Ottiene lo stile di bande di riga pari. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Ottiene lo stile della prima colonna. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Ottiene lo stile della prima riga. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Recupera a[`ConditionalStyle`](../conditionalstyle/) oggetto per tipo di stile condizionale. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Ottiene lo stile dell'ultima colonna. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Ottiene lo stile dell'ultima riga. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Ottiene lo stile di raggruppamento delle colonne dispari. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Ottiene lo stile di righe dispari. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Ottiene lo stile della cella in alto a sinistra. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Ottiene lo stile della cella in alto a destra. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Cancella tutti gli stili condizionali dello stile tabella. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli stili condizionali nella raccolta. |

### Osservazioni

Non è possibile aggiungere o rimuovere elementi da questa raccolta. Contiene un insieme permanente di elementi: un elemento per ogni valore di[`ConditionalStyleType`](../conditionalstyletype/) tipo di enumerazione.

### Esempi

Mostra come lavorare con determinati stili di area di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Crea uno stile tabella personalizzato.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Gli stili condizionali sono modifiche alla formattazione che interessano solo alcune celle della tabella
// basato su un predicato, ad esempio le celle nell'ultima riga.
// Di seguito sono riportati tre modi per accedere agli stili condizionali di uno stile tabella dalla raccolta "ConditionalStyles".
// 1 - Per tipo di stile:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Per indice:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Come proprietà:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Applica il riempimento e la formattazione del testo agli stili condizionali.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Elenca tutte le possibili condizioni di stile.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Applica lo stile personalizzato, che contiene tutti gli stili condizionali, alla tabella.
table.Style = tableStyle;

// Il nostro stile applica alcuni stili condizionali per impostazione predefinita.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Dovremo abilitare noi stessi tutti gli altri stili tramite la proprietà "StyleOptions".
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Guarda anche

* class [ConditionalStyle](../conditionalstyle/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


