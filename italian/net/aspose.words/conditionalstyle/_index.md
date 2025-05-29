---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.ConditionalStyle per la formattazione avanzata delle tabelle. Arricchisci i tuoi documenti con stili dinamici e migliora la leggibilità senza sforzo.
type: docs
weight: 510
url: /it/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Rappresenta una formattazione speciale applicata ad alcune aree di una tabella con stile tabella assegnato.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public sealed class ConditionalStyle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Ottiene la raccolta di bordi di cella predefiniti per lo stile condizionale. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sotto il contenuto delle celle della tabella. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Ottiene la formattazione del carattere dello stile condizionale. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a sinistra del contenuto delle celle della tabella. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Ottiene la formattazione del paragrafo dello stile condizionale. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere a destra del contenuto delle celle della tabella. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Ottiene un[`Shading`](../shading/) oggetto che fa riferimento alla formattazione dell'ombreggiatura per questo stile condizionale. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Ottiene o imposta la quantità di spazio (in punti) da aggiungere sopra il contenuto delle celle della tabella. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Ottiene l'area della tabella a cui si riferisce questo stile condizionale. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Cancella la formattazione di questo stile condizionale. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Confronta questo stile condizionale con l'oggetto specificato. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Calcola il codice hash per questo oggetto. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
