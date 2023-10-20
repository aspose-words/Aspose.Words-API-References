---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words per .NET
description: TableStyle ColumnStripe proprietà. Ottiene o imposta un numero di colonne da includere nella suddivisione quando lo stile specifica la suddivisione delle colonne pari/dispari in C#.
type: docs
weight: 70
url: /it/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

Ottiene o imposta un numero di colonne da includere nella suddivisione quando lo stile specifica la suddivisione delle colonne pari/dispari.

```csharp
public int ColumnStripe { get; set; }
```

## Esempi

Mostra come creare stili di tabella condizionali che si alternano tra le righe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo configurare uno stile condizionale di una tabella per applicare un colore diverso alla riga/colonna,
// in base al fatto che la riga/colonna sia pari o dispari, creando uno schema di colori alternati.
// Possiamo anche applicare un numero n alla fasciatura di riga/colonna,
// significa che il colore si alterna dopo ogni n righe/colonne invece di una.
// Crea una tabella in cui singole colonne e righe uniranno le colonne in tre.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Applica uno stile di linea a tutti i bordi della tabella.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Imposta i due colori, che si alterneranno ogni 3 righe.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Imposta un colore da applicare a ogni colonna pari, che sovrascriverà qualsiasi colorazione di riga personalizzata.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// La proprietà "StyleOptions" abilita la suddivisione delle righe per impostazione predefinita.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Utilizza la proprietà "StyleOptions" anche per abilitare il raggruppamento delle colonne.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### Guarda anche

* class [TableStyle](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
