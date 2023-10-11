---
title: Enum ConditionalStyleType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ConditionalStyleType enum. Rappresenta le possibili aree della tabella in cui è possibile definire la formattazione condizionale in uno stile di tabella.
type: docs
weight: 330
url: /it/net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Rappresenta le possibili aree della tabella in cui è possibile definire la formattazione condizionale in uno stile di tabella.

```csharp
public enum ConditionalStyleType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FirstRow | `0` | Specifica la formattazione della prima riga di una tabella. |
| FirstColumn | `1` | Specifica la formattazione della prima colonna di una tabella. |
| LastRow | `2` | Specifica la formattazione dell'ultima riga di una tabella. |
| LastColumn | `3` | Specifica la formattazione dell'ultima colonna di una tabella. |
| OddRowBanding | `4` | Specifica la formattazione della striscia di riga con numeri dispari. |
| OddColumnBanding | `5` | Specifica la formattazione della striscia di colonna con numero dispari. |
| EvenRowBanding | `6` | Specifica la formattazione della striscia di riga con numero pari. |
| EvenColumnBanding | `7` | Specifica la formattazione della striscia di colonna con numero pari. |
| TopLeftCell | `8` | Specifica la formattazione della cella in alto a sinistra di una tabella. |
| TopRightCell | `9` | Specifica la formattazione della cella in alto a destra di una tabella. |
| BottomLeftCell | `10` | Specifica la formattazione della cella in basso a sinistra di una tabella. |
| BottomRightCell | `11` | Specifica la formattazione della cella in basso a destra di una tabella. |

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

// Crea uno stile di tabella personalizzato.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Gli stili condizionali sono modifiche alla formattazione che influiscono solo su alcune celle della tabella
// basato su un predicato, ad esempio le celle nell'ultima riga.
// Di seguito sono riportati tre modi per accedere agli stili condizionali di uno stile di tabella dalla raccolta "ConditionalStyles".
// 1 - Per tipo di stile:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - Per indice:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Come immobile:
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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


