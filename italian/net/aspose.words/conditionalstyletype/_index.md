---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ConditionalStyleType per definire la formattazione dinamica delle tabelle. Migliora gli stili dei tuoi documenti con opzioni flessibili e condizionali!
type: docs
weight: 530
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
| OddRowBanding | `4` | Specifica la formattazione della striscia di righe dispari. |
| OddColumnBanding | `5` | Specifica la formattazione della striscia di colonne dispari. |
| EvenRowBanding | `6` | Specifica la formattazione della striscia di righe pari. |
| EvenColumnBanding | `7` | Specifica la formattazione della striscia di colonne pari. |
| TopLeftCell | `8` | Specifica la formattazione della cella in alto a sinistra di una tabella. |
| TopRightCell | `9` | Specifica la formattazione della cella in alto a destra di una tabella. |
| BottomLeftCell | `10` | Specifica la formattazione della cella in basso a sinistra di una tabella. |
| BottomRightCell | `11` | Specifica la formattazione della cella in basso a destra di una tabella. |

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
