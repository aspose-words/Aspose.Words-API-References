---
title: Class ConditionalStyle
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ConditionalStyle classe. Rappresenta una formattazione speciale applicata ad unarea di una tabella con uno stile di tabella assegnato.
type: docs
weight: 300
url: /it/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Rappresenta una formattazione speciale applicata ad un'area di una tabella con uno stile di tabella assegnato.

```csharp
public sealed class ConditionalStyle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Ottiene la raccolta dei bordi delle celle predefiniti per lo stile condizionale. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle della tabella. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Ottiene la formattazione dei caratteri dello stile condizionale. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Ottiene la formattazione del paragrafo dello stile condizionale. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle della tabella. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Ottiene a[`Shading`](../shading/) oggetto che fa riferimento alla formattazione dell'ombreggiatura per questo stile condizionale. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Ottiene l'area della tabella a cui si riferisce questo stile condizionale. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Cancella la formattazione di questo stile condizionale. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(object) |  |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Calcola il codice hash per questo oggetto. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


