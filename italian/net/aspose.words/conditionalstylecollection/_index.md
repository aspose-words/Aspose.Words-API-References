---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.ConditionalStyleCollection per gestire efficacemente gli oggetti ConditionalStyle, migliorando la formattazione e la personalizzazione dei documenti.
type: docs
weight: 520
url: /it/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Rappresenta una raccolta di[`ConditionalStyle`](../conditionalstyle/) oggetti.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Ottiene lo stile della cella in basso a sinistra. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Ottiene lo stile della cella in basso a destra. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Ottiene il numero di stili condizionali nella raccolta. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Ottiene lo stile di suddivisione in colonne pari. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Ottiene lo stile di bande di righe pari. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Ottiene lo stile della prima colonna. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Ottiene lo stile della prima riga. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Recupera un[`ConditionalStyle`](../conditionalstyle/) oggetto per tipo di stile condizionale. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Ottiene lo stile dell'ultima colonna. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Ottiene lo stile dell'ultima riga. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Ottiene lo stile di suddivisione delle colonne dispari. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Ottiene lo stile di suddivisione delle righe dispari. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Ottiene lo stile della cella in alto a sinistra. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Ottiene lo stile della cella in alto a destra. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Cancella tutti gli stili condizionali dello stile della tabella. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli stili condizionali nella raccolta. |

## Osservazioni

Non è possibile aggiungere o rimuovere elementi da questa raccolta. Contiene un set permanente di elementi: un elemento per ogni valore di[`ConditionalStyleType`](../conditionalstyletype/) tipo di enumerazione.

## Esempi

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

// Crea uno stile di tabella personalizzato.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Gli stili condizionali sono modifiche di formattazione che interessano solo alcune celle della tabella
// in base a un predicato, ad esempio se le celle si trovano nell'ultima riga.
// Di seguito sono riportati tre modi per accedere agli stili condizionali di uno stile di tabella dalla raccolta "ConditionalStyles".
// 1 - Per tipo di stile:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Per indice:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Come proprietà:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Applica la spaziatura interna e la formattazione del testo agli stili condizionali.
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

// Applica alla tabella lo stile personalizzato che contiene tutti gli stili condizionali.
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
